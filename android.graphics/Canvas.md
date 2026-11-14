# Canvas

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Canvas

Kotlin| [Java](https://developer.android.com/reference/android/graphics/Canvas "View this page in Java") 

```
open class Canvas
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.graphics.Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas#) |

| Known Direct Subclasses [RecordingCanvas](https://developer.android.com/reference/kotlin/android/graphics/RecordingCanvas) |----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------| | [RecordingCanvas](https://developer.android.com/reference/kotlin/android/graphics/RecordingCanvas) | A Canvas implementation that records view system drawing operations for deferred rendering. | |

The Canvas class holds the "draw" calls. To draw something, you need 4 basic components: A Bitmap to hold the pixels, a Canvas to host the draw calls (writing into the bitmap), a drawing primitive (e.g. Rect, Path, text, Bitmap), and a paint (to describe the colors and styles for the drawing).
|
| ### Developer Guides
|
| For more information about how to use Canvas, read the [Canvas and Drawables](https://developer.android.com/guide/topics/graphics/2d-graphics.html) developer guide.

<br />

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [EdgeType](https://developer.android.com/reference/kotlin/android/graphics/Canvas.EdgeType) Constant values used as parameters to`quickReject()`calls. |
| | [VertexMode](https://developer.android.com/reference/kotlin/android/graphics/Canvas.VertexMode) <br /> |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALL_SAVE_FLAG](https://developer.android.com/reference/kotlin/android/graphics/Canvas#ALL_SAVE_FLAG:kotlin.Int) Restore everything when restore() is called (standard save flags). |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas#Canvas())`()` Construct an empty raster canvas. |
| [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas#Canvas(android.graphics.Bitmap))`(`bitmap:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap)`)` Construct a canvas with the specified bitmap to draw into. |

| Public methods ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [clipOutPath](https://developer.android.com/reference/kotlin/android/graphics/Canvas#clipOutPath(android.graphics.Path))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path)`)` Set the clip to the difference of the current clip and the specified path. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [clipOutRect](https://developer.android.com/reference/kotlin/android/graphics/Canvas#clipOutRect(android.graphics.Rect))`(`rect:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect)`)` Set the clip to the difference of the current clip and the specified rectangle, which is expressed in local coordinates. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [clipOutRect](https://developer.android.com/reference/kotlin/android/graphics/Canvas#clipOutRect(android.graphics.RectF))`(`rect:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)`)` Set the clip to the difference of the current clip and the specified rectangle, which is expressed in local coordinates. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [clipOutRect](https://developer.android.com/reference/kotlin/android/graphics/Canvas#clipOutRect(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`left:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `top:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `right:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bottom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the clip to the difference of the current clip and the specified rectangle, which is expressed in local coordinates. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [clipOutRect](https://developer.android.com/reference/kotlin/android/graphics/Canvas#clipOutRect(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the clip to the difference of the current clip and the specified rectangle, which is expressed in local coordinates. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clipOutShader](https://developer.android.com/reference/kotlin/android/graphics/Canvas#clipOutShader(android.graphics.Shader))`(`shader:` ` [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader)`)` Set the clip to the difference of the current clip and the shader. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [clipPath](https://developer.android.com/reference/kotlin/android/graphics/Canvas#clipPath(android.graphics.Path))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path)`)` Intersect the current clip with the specified path. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [clipPath](https://developer.android.com/reference/kotlin/android/graphics/Canvas#clipPath(android.graphics.Path,%20android.graphics.Region.Op))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path)`, `op:` ` [Region.Op](https://developer.android.com/reference/kotlin/android/graphics/Region.Op)`)` Modify the current clip with the specified path. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [clipRect](https://developer.android.com/reference/kotlin/android/graphics/Canvas#clipRect(android.graphics.Rect))`(`rect:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect)`)` Intersect the current clip with the specified rectangle, which is expressed in local coordinates. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [clipRect](https://developer.android.com/reference/kotlin/android/graphics/Canvas#clipRect(android.graphics.Rect,%20android.graphics.Region.Op))`(`rect:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect)`, `op:` ` [Region.Op](https://developer.android.com/reference/kotlin/android/graphics/Region.Op)`)` Modify the current clip with the specified rectangle, which is expressed in local coordinates. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [clipRect](https://developer.android.com/reference/kotlin/android/graphics/Canvas#clipRect(android.graphics.RectF))`(`rect:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)`)` Intersect the current clip with the specified rectangle, which is expressed in local coordinates. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [clipRect](https://developer.android.com/reference/kotlin/android/graphics/Canvas#clipRect(android.graphics.RectF,%20android.graphics.Region.Op))`(`rect:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)`, `op:` ` [Region.Op](https://developer.android.com/reference/kotlin/android/graphics/Region.Op)`)` Modify the current clip with the specified rectangle. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [clipRect](https://developer.android.com/reference/kotlin/android/graphics/Canvas#clipRect(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`left:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `top:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `right:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bottom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Intersect the current clip with the specified rectangle, which is expressed in local coordinates. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [clipRect](https://developer.android.com/reference/kotlin/android/graphics/Canvas#clipRect(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Region.Op))`(`left:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `top:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `right:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bottom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `op:` ` [Region.Op](https://developer.android.com/reference/kotlin/android/graphics/Region.Op)`)` Modify the current clip with the specified rectangle, which is expressed in local coordinates. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [clipRect](https://developer.android.com/reference/kotlin/android/graphics/Canvas#clipRect(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Intersect the current clip with the specified rectangle, which is expressed in local coordinates. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clipShader](https://developer.android.com/reference/kotlin/android/graphics/Canvas#clipShader(android.graphics.Shader))`(`shader:` ` [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader)`)` Intersect the current clip with the specified shader. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [concat](https://developer.android.com/reference/kotlin/android/graphics/Canvas#concat(android.graphics.Matrix))`(`matrix:` ` [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix)?`)` Preconcat the current matrix with the specified matrix. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [concat](https://developer.android.com/reference/kotlin/android/graphics/Canvas#concat(android.graphics.Matrix44))`(`m:` ` [Matrix44](https://developer.android.com/reference/kotlin/android/graphics/Matrix44)?`)` Preconcat the current matrix with the specified matrix. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [disableZ](https://developer.android.com/reference/kotlin/android/graphics/Canvas#disableZ())`()` Disables Z support, preventing any RenderNodes drawn after this point from being visually reordered or having shadows rendered. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawARGB](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawARGB(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`a:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `r:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `g:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Fill the entire canvas' bitmap (restricted to the current clip) with the specified ARGB color, using srcover porterduff mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawArc](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawArc(android.graphics.RectF,%20kotlin.Float,%20kotlin.Float,%20kotlin.Boolean,%20android.graphics.Paint))`(`oval:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)`, `startAngle:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `sweepAngle:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `useCenter:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw the specified arc, which will be scaled to fit inside the specified oval. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawArc](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawArc(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Boolean,%20android.graphics.Paint))`(`left:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `top:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `right:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bottom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `startAngle:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `sweepAngle:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `useCenter:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw the specified arc, which will be scaled to fit inside the specified oval. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawBitmap](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawBitmap(android.graphics.Bitmap,%20android.graphics.Matrix,%20android.graphics.Paint))`(`bitmap:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap)`, `matrix:` ` [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?`)` Draw the bitmap using the specified matrix. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawBitmap](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawBitmap(android.graphics.Bitmap,%20android.graphics.Rect,%20android.graphics.Rect,%20android.graphics.Paint))`(`bitmap:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap)`, `src:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect)?`, `dst:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?`)` Draw the specified bitmap, scaling/translating automatically to fill the destination rectangle. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawBitmap](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawBitmap(android.graphics.Bitmap,%20android.graphics.Rect,%20android.graphics.RectF,%20android.graphics.Paint))`(`bitmap:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap)`, `src:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect)?`, `dst:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?`)` Draw the specified bitmap, scaling/translating automatically to fill the destination rectangle. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawBitmap](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawBitmap(android.graphics.Bitmap,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Paint))`(`bitmap:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap)`, `left:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `top:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?`)` Draw the specified bitmap, with its top/left corner at (x,y), using the specified paint, transformed by the current matrix. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawBitmap](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawBitmap(kotlin.IntArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.graphics.Paint))`(`colors:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `stride:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `hasAlpha:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?`)` Treat the specified array of colors as a bitmap, and draw it. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawBitmap](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawBitmap(kotlin.IntArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.graphics.Paint))`(`colors:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `stride:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `y:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `hasAlpha:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?`)` Legacy version of drawBitmap(int\[\] colors, ...) that took ints for x,y |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawBitmapMesh](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawBitmapMesh(android.graphics.Bitmap,%20kotlin.Int,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int,%20kotlin.IntArray,%20kotlin.Int,%20android.graphics.Paint))`(`bitmap:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap)`, `meshWidth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `meshHeight:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `verts:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)`, `vertOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `colors:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?`, `colorOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?`)` Draw the bitmap through the mesh, where mesh vertices are evenly distributed across the bitmap. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawCircle](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawCircle(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Paint))`(`cx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `cy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `radius:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw the specified circle using the specified paint. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawColor](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawColor(kotlin.Int))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Fill the entire canvas' bitmap (restricted to the current clip) with the specified color, using srcover porterduff mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawColor](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawColor(kotlin.Int,%20android.graphics.BlendMode))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mode:` ` [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode)`)` Fill the entire canvas' bitmap (restricted to the current clip) with the specified color and blendmode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawColor](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawColor(kotlin.Int,%20android.graphics.PorterDuff.Mode))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mode:` ` [PorterDuff.Mode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode)`)` Fill the entire canvas' bitmap (restricted to the current clip) with the specified color and porter-duff xfermode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawColor](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawColor(kotlin.Long))`(`color:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Fill the entire canvas' bitmap (restricted to the current clip) with the specified color, using srcover porterduff mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawColor](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawColor(kotlin.Long,%20android.graphics.BlendMode))`(`color:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `mode:` ` [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode)`)` Fill the entire canvas' bitmap (restricted to the current clip) with the specified color and blendmode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawDoubleRoundRect](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawDoubleRoundRect(android.graphics.RectF,%20kotlin.Float,%20kotlin.Float,%20android.graphics.RectF,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Paint))`(`outer:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)`, `outerRx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `outerRy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `inner:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)`, `innerRx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `innerRy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draws a double rounded rectangle using the specified paint. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawDoubleRoundRect](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawDoubleRoundRect(android.graphics.RectF,%20kotlin.FloatArray,%20android.graphics.RectF,%20kotlin.FloatArray,%20android.graphics.Paint))`(`outer:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)`, `outerRadii:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)`, `inner:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)`, `innerRadii:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draws a double rounded rectangle using the specified paint. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawGlyphs](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawGlyphs(kotlin.IntArray,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int,%20kotlin.Int,%20android.graphics.fonts.Font,%20android.graphics.Paint))`(`glyphIds:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`, `glyphIdOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `positions:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)`, `positionOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `glyphCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `font:` ` [Font](https://developer.android.com/reference/kotlin/android/graphics/fonts/Font)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw array of glyphs with specified font. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawLine](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawLine(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Paint))`(`startX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `startY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `stopX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `stopY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw a line segment with the specified start and stop x,y coordinates, using the specified paint. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawLines](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawLines(kotlin.FloatArray,%20android.graphics.Paint))`(`pts:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawLines](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawLines(kotlin.FloatArray,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Paint))`(`pts:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw a series of lines. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawMesh](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawMesh(android.graphics.Mesh,%20android.graphics.BlendMode,%20android.graphics.Paint))`(`mesh:` ` [Mesh](https://developer.android.com/reference/kotlin/android/graphics/Mesh)`, `blendMode:` ` [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode)?`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draws a mesh object to the screen. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawOval](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawOval(android.graphics.RectF,%20android.graphics.Paint))`(`oval:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw the specified oval using the specified paint. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawOval](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawOval(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Paint))`(`left:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `top:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `right:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bottom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw the specified oval using the specified paint. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawPaint](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawPaint(android.graphics.Paint))`(`paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Fill the entire canvas' bitmap (restricted to the current clip) with the specified paint. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawPatch](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawPatch(android.graphics.NinePatch,%20android.graphics.Rect,%20android.graphics.Paint))`(`patch:` ` [NinePatch](https://developer.android.com/reference/kotlin/android/graphics/NinePatch)`, `dst:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?`)` Draws the specified bitmap as an N-patch (most often, a 9-patch.) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawPatch](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawPatch(android.graphics.NinePatch,%20android.graphics.RectF,%20android.graphics.Paint))`(`patch:` ` [NinePatch](https://developer.android.com/reference/kotlin/android/graphics/NinePatch)`, `dst:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?`)` Draws the specified bitmap as an N-patch (most often, a 9-patch.) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawPath](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawPath(android.graphics.Path,%20android.graphics.Paint))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw the specified path using the specified paint. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawPicture](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawPicture(android.graphics.Picture))`(`picture:` ` [Picture](https://developer.android.com/reference/kotlin/android/graphics/Picture)`)` Save the canvas state, draw the picture, and restore the canvas state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawPicture](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawPicture(android.graphics.Picture,%20android.graphics.Rect))`(`picture:` ` [Picture](https://developer.android.com/reference/kotlin/android/graphics/Picture)`, `dst:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect)`)` Draw the picture, stretched to fit into the dst rectangle. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawPicture](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawPicture(android.graphics.Picture,%20android.graphics.RectF))`(`picture:` ` [Picture](https://developer.android.com/reference/kotlin/android/graphics/Picture)`, `dst:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)`)` Draw the picture, stretched to fit into the dst rectangle. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawPoint](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawPoint(kotlin.Float,%20kotlin.Float,%20android.graphics.Paint))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Helper for drawPoints() for drawing a single point. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawPoints](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawPoints(kotlin.FloatArray,%20android.graphics.Paint))`(`pts:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Helper for drawPoints() that assumes you want to draw the entire array |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawPoints](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawPoints(kotlin.FloatArray,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Paint))`(`pts:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw a series of points. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawPosText](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawPosText(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.FloatArray,%20android.graphics.Paint))`(`text:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pos:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw the text in the array, with each character's origin specified by the pos array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawPosText](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawPosText(kotlin.String,%20kotlin.FloatArray,%20android.graphics.Paint))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `pos:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw the text in the array, with each character's origin specified by the pos array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawRGB](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawRGB(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`r:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `g:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Fill the entire canvas' bitmap (restricted to the current clip) with the specified RGB color, using srcover porterduff mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawRect](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawRect(android.graphics.Rect,%20android.graphics.Paint))`(`r:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw the specified Rect using the specified Paint. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawRect](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawRect(android.graphics.RectF,%20android.graphics.Paint))`(`rect:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw the specified Rect using the specified paint. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawRect](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawRect(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Paint))`(`left:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `top:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `right:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bottom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw the specified Rect using the specified paint. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawRegion](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawRegion(android.graphics.Region,%20android.graphics.Paint))`(`region:` ` [Region](https://developer.android.com/reference/kotlin/android/graphics/Region)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draws the given region using the given paint. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawRenderNode](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawRenderNode(android.graphics.RenderNode))`(`renderNode:` ` [RenderNode](https://developer.android.com/reference/kotlin/android/graphics/RenderNode)`)` Draws the given RenderNode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawRoundRect](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawRoundRect(android.graphics.RectF,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Paint))`(`rect:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)`, `rx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `ry:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw the specified round-rect using the specified paint. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawRoundRect](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawRoundRect(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Paint))`(`left:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `top:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `right:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bottom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `rx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `ry:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw the specified round-rect using the specified paint. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawText](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawText(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Paint))`(`text:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw the text, with origin at (x,y), using the specified paint. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawText](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawText(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Paint))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw the specified range of text, specified by start/end, with its origin at (x,y), in the specified Paint. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawText](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawText(kotlin.String,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Paint))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw the text, with origin at (x,y), using the specified paint. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawText](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawText(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Paint))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw the text, with origin at (x,y), using the specified paint. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawTextOnPath](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawTextOnPath(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Path,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Paint))`(`text:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path)`, `hOffset:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `vOffset:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw the text, with origin at (x,y), using the specified paint, along the specified path. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawTextOnPath](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawTextOnPath(kotlin.String,%20android.graphics.Path,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Paint))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path)`, `hOffset:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `vOffset:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw the text, with origin at (x,y), using the specified paint, along the specified path. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawTextRun](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawTextRun(android.graphics.text.MeasuredText,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20kotlin.Boolean,%20android.graphics.Paint))`(`text:` ` [MeasuredText](https://developer.android.com/reference/kotlin/android/graphics/text/MeasuredText)`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `contextStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `contextEnd:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `isRtl:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw a run of text, all in a single direction, with optional context for complex text shaping. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawTextRun](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawTextRun(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20kotlin.Boolean,%20android.graphics.Paint))`(`text:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `contextIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `contextCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `isRtl:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw a run of text, all in a single direction, with optional context for complex text shaping. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawTextRun](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawTextRun(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20kotlin.Boolean,%20android.graphics.Paint))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `contextStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `contextEnd:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `isRtl:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw a run of text, all in a single direction, with optional context for complex text shaping. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawVertices](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawVertices(android.graphics.Canvas.VertexMode,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int,%20kotlin.IntArray,%20kotlin.Int,%20kotlin.ShortArray,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Paint))`(`mode:` ` [Canvas.VertexMode](https://developer.android.com/reference/kotlin/android/graphics/Canvas.VertexMode)`, `vertexCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `verts:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)`, `vertOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `texs:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?`, `texOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `colors:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?`, `colorOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `indices:` ` [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)?`, `indexOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `indexCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)`)` Draw the array of vertices, interpreted as triangles (based on mode). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [enableZ](https://developer.android.com/reference/kotlin/android/graphics/Canvas#enableZ())`()` Enables Z support which defaults to disabled. |
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect) | [getClipBounds](https://developer.android.com/reference/kotlin/android/graphics/Canvas#getClipBounds())`()` Retrieve the bounds of the current clip (in local coordinates). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getClipBounds](https://developer.android.com/reference/kotlin/android/graphics/Canvas#getClipBounds(android.graphics.Rect))`(`bounds:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect)`)` Return the bounds of the current clip (in local coordinates) in the bounds parameter, and return true if it is non-empty. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDensity](https://developer.android.com/reference/kotlin/android/graphics/Canvas#getDensity())`()` Returns the target density of the canvas. |
| open [DrawFilter](https://developer.android.com/reference/kotlin/android/graphics/DrawFilter)? | [getDrawFilter](https://developer.android.com/reference/kotlin/android/graphics/Canvas#getDrawFilter())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeight](https://developer.android.com/reference/kotlin/android/graphics/Canvas#getHeight())`()` Returns the height of the current drawing layer |
| [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix) | [getMatrix](https://developer.android.com/reference/kotlin/android/graphics/Canvas#getMatrix())`()` Return a new matrix with a copy of the canvas' current transformation matrix. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getMatrix](https://developer.android.com/reference/kotlin/android/graphics/Canvas#getMatrix(android.graphics.Matrix))`(`ctm:` ` [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix)`)` Return, in ctm, the current transformation matrix. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaximumBitmapHeight](https://developer.android.com/reference/kotlin/android/graphics/Canvas#getMaximumBitmapHeight())`()` Returns the maximum allowed height for bitmaps drawn with this canvas. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaximumBitmapWidth](https://developer.android.com/reference/kotlin/android/graphics/Canvas#getMaximumBitmapWidth())`()` Returns the maximum allowed width for bitmaps drawn with this canvas. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSaveCount](https://developer.android.com/reference/kotlin/android/graphics/Canvas#getSaveCount())`()` Returns the number of matrix/clip states on the Canvas' private stack. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidth](https://developer.android.com/reference/kotlin/android/graphics/Canvas#getWidth())`()` Returns the width of the current drawing layer |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHardwareAccelerated](https://developer.android.com/reference/kotlin/android/graphics/Canvas#isHardwareAccelerated())`()` Indicates whether this Canvas uses hardware acceleration. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpaque](https://developer.android.com/reference/kotlin/android/graphics/Canvas#isOpaque())`()` Return true if the device that the current layer draws into is opaque (that is, it does not support per-pixel alpha). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [quickReject](https://developer.android.com/reference/kotlin/android/graphics/Canvas#quickReject(android.graphics.Path))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path)`)` Return true if the specified path, after being transformed by the current matrix, would lie completely outside of the current clip. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [quickReject](https://developer.android.com/reference/kotlin/android/graphics/Canvas#quickReject(android.graphics.Path,%20android.graphics.Canvas.EdgeType))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path)`, `type:` ` [Canvas.EdgeType](https://developer.android.com/reference/kotlin/android/graphics/Canvas.EdgeType)`)` Return true if the specified path, after being transformed by the current matrix, would lie completely outside of the current clip. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [quickReject](https://developer.android.com/reference/kotlin/android/graphics/Canvas#quickReject(android.graphics.RectF))`(`rect:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)`)` Return true if the specified rectangle, after being transformed by the current matrix, would lie completely outside of the current clip. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [quickReject](https://developer.android.com/reference/kotlin/android/graphics/Canvas#quickReject(android.graphics.RectF,%20android.graphics.Canvas.EdgeType))`(`rect:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)`, `type:` ` [Canvas.EdgeType](https://developer.android.com/reference/kotlin/android/graphics/Canvas.EdgeType)`)` Return true if the specified rectangle, after being transformed by the current matrix, would lie completely outside of the current clip. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [quickReject](https://developer.android.com/reference/kotlin/android/graphics/Canvas#quickReject(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`left:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `top:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `right:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bottom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Return true if the specified rectangle, after being transformed by the current matrix, would lie completely outside of the current clip. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [quickReject](https://developer.android.com/reference/kotlin/android/graphics/Canvas#quickReject(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Canvas.EdgeType))`(`left:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `top:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `right:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bottom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `type:` ` [Canvas.EdgeType](https://developer.android.com/reference/kotlin/android/graphics/Canvas.EdgeType)`)` Return true if the specified rectangle, after being transformed by the current matrix, would lie completely outside of the current clip. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restore](https://developer.android.com/reference/kotlin/android/graphics/Canvas#restore())`()` This call balances a previous call to save(), and is used to remove all modifications to the matrix/clip state since the last save call. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreToCount](https://developer.android.com/reference/kotlin/android/graphics/Canvas#restoreToCount(kotlin.Int))`(`saveCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Efficient way to pop any calls to save() that happened after the save count reached saveCount. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [rotate](https://developer.android.com/reference/kotlin/android/graphics/Canvas#rotate(kotlin.Float))`(`degrees:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Preconcat the current matrix with the specified rotation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [rotate](https://developer.android.com/reference/kotlin/android/graphics/Canvas#rotate(kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`degrees:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `px:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `py:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Preconcat the current matrix with the specified rotation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [save](https://developer.android.com/reference/kotlin/android/graphics/Canvas#save())`()` Saves the current matrix and clip onto a private stack. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [saveLayer](https://developer.android.com/reference/kotlin/android/graphics/Canvas#saveLayer(android.graphics.RectF,%20android.graphics.Paint))`(`bounds:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)?`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?`)` This behaves the same as save(), but in addition it allocates and redirects drawing to an offscreen rendering target. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [saveLayer](https://developer.android.com/reference/kotlin/android/graphics/Canvas#saveLayer(android.graphics.RectF,%20android.graphics.Paint,%20kotlin.Int))`(`bounds:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)?`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?`, `saveFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This behaves the same as save(), but in addition it allocates and redirects drawing to an offscreen bitmap. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [saveLayer](https://developer.android.com/reference/kotlin/android/graphics/Canvas#saveLayer(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Paint))`(`left:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `top:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `right:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bottom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?`)` Convenience for [saveLayer(android.graphics.RectF,android.graphics.Paint)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#saveLayer(android.graphics.RectF,%20android.graphics.Paint))that takes the four float coordinates of the bounds rectangle. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [saveLayer](https://developer.android.com/reference/kotlin/android/graphics/Canvas#saveLayer(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Paint,%20kotlin.Int))`(`left:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `top:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `right:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bottom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?`, `saveFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Helper version of saveLayer() that takes 4 values rather than a RectF. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [saveLayerAlpha](https://developer.android.com/reference/kotlin/android/graphics/Canvas#saveLayerAlpha(android.graphics.RectF,%20kotlin.Int))`(`bounds:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)?`, `alpha:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Convenience for [saveLayer(android.graphics.RectF,android.graphics.Paint)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#saveLayer(android.graphics.RectF,%20android.graphics.Paint))but instead of taking a entire Paint object it takes only the`alpha`parameter. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [saveLayerAlpha](https://developer.android.com/reference/kotlin/android/graphics/Canvas#saveLayerAlpha(android.graphics.RectF,%20kotlin.Int,%20kotlin.Int))`(`bounds:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)?`, `alpha:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `saveFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This behaves the same as save(), but in addition it allocates and redirects drawing to an offscreen bitmap. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [saveLayerAlpha](https://developer.android.com/reference/kotlin/android/graphics/Canvas#saveLayerAlpha(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int))`(`left:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `top:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `right:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bottom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `alpha:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Convenience for [saveLayerAlpha(android.graphics.RectF,int)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#saveLayerAlpha(android.graphics.RectF,%20kotlin.Int))that takes the four float coordinates of the bounds rectangle. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [saveLayerAlpha](https://developer.android.com/reference/kotlin/android/graphics/Canvas#saveLayerAlpha(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int,%20kotlin.Int))`(`left:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `top:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `right:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bottom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `alpha:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `saveFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Helper for saveLayerAlpha() that takes 4 values instead of a RectF. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scale](https://developer.android.com/reference/kotlin/android/graphics/Canvas#scale(kotlin.Float,%20kotlin.Float))`(`sx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `sy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Preconcat the current matrix with the specified scale. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scale](https://developer.android.com/reference/kotlin/android/graphics/Canvas#scale(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`sx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `sy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `px:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `py:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Preconcat the current matrix with the specified scale. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBitmap](https://developer.android.com/reference/kotlin/android/graphics/Canvas#setBitmap(android.graphics.Bitmap))`(`bitmap:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap)?`)` Specify a bitmap for the canvas to draw into. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDensity](https://developer.android.com/reference/kotlin/android/graphics/Canvas#setDensity(kotlin.Int))`(`density:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specifies the density for this Canvas' backing bitmap. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDrawFilter](https://developer.android.com/reference/kotlin/android/graphics/Canvas#setDrawFilter(android.graphics.DrawFilter))`(`filter:` ` [DrawFilter](https://developer.android.com/reference/kotlin/android/graphics/DrawFilter)?`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMatrix](https://developer.android.com/reference/kotlin/android/graphics/Canvas#setMatrix(android.graphics.Matrix))`(`matrix:` ` [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix)?`)` Completely replace the current matrix with the specified matrix. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [skew](https://developer.android.com/reference/kotlin/android/graphics/Canvas#skew(kotlin.Float,%20kotlin.Float))`(`sx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `sy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Preconcat the current matrix with the specified skew. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [translate](https://developer.android.com/reference/kotlin/android/graphics/Canvas#translate(kotlin.Float,%20kotlin.Float))`(`dx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `dy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Preconcat the current matrix with the specified translation |

## Constants

### ALL_SAVE_FLAG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALL_SAVE_FLAG: Int
```

Restore everything when restore() is called (standard save flags).

**Note:** for performance reasons, it is strongly recommended to pass this - the complete set of flags - to any call to`saveLayer()`and`saveLayerAlpha()`variants.

**Note:**all methods that accept this flag have flagless versions that are equivalent to passing this flag. 

 Value: 31

## Public constructors

### Canvas

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Canvas()
```

Construct an empty raster canvas. Use setBitmap() to specify a bitmap to draw into. The initial target density is [Bitmap.DENSITY_NONE](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#DENSITY_NONE:kotlin.Int); this will typically be replaced when a target bitmap is set for the canvas. 

### Canvas

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Canvas(bitmap: Bitmap)
```

Construct a canvas with the specified bitmap to draw into. The bitmap must be mutable.

The initial target density of the canvas is the same as the given bitmap's density.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bitmap` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap):Specifies a mutable bitmap for the canvas to draw into. This value cannot be`null`. |

## Public methods

### clipOutPath

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clipOutPath(path: Path): Boolean
```

Set the clip to the difference of the current clip and the specified path.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path):The path used in the difference operation This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the resulting clip is non-empty |

### clipOutRect

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clipOutRect(rect: Rect): Boolean
```

Set the clip to the difference of the current clip and the specified rectangle, which is expressed in local coordinates.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rect` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect):The rectangle to perform a difference op with the current clip. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the resulting clip is non-empty |

### clipOutRect

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clipOutRect(rect: RectF): Boolean
```

Set the clip to the difference of the current clip and the specified rectangle, which is expressed in local coordinates.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rect` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF):The rectangle to perform a difference op with the current clip. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the resulting clip is non-empty |

### clipOutRect

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clipOutRect(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float
): Boolean
```

Set the clip to the difference of the current clip and the specified rectangle, which is expressed in local coordinates.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `left` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The left side of the rectangle used in the difference operation |
| `top` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The top of the rectangle used in the difference operation |
| `right` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The right side of the rectangle used in the difference operation |
| `bottom` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The bottom of the rectangle used in the difference operation |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the resulting clip is non-empty |

### clipOutRect

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clipOutRect(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Boolean
```

Set the clip to the difference of the current clip and the specified rectangle, which is expressed in local coordinates.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The left side of the rectangle used in the difference operation |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The top of the rectangle used in the difference operation |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The right side of the rectangle used in the difference operation |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The bottom of the rectangle used in the difference operation |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the resulting clip is non-empty |

### clipOutShader

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clipOutShader(shader: Shader): Unit
```

Set the clip to the difference of the current clip and the shader. The shader will be treated as an alpha mask, taking the difference of the two.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `shader` | [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader):The shader to intersect with the current clip This value cannot be`null`. |

### clipPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clipPath(path: Path): Boolean
```

Intersect the current clip with the specified path.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path):The path to intersect with the current clip This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the resulting clip is non-empty |

### clipPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clipPath(
    path: Path, 
    op: Region.Op
): Boolean
```

**Deprecated:** *Region.Op values other than [Region.Op.INTERSECT](https://developer.android.com/reference/kotlin/android/graphics/Region.Op) and [Region.Op.DIFFERENCE](https://developer.android.com/reference/kotlin/android/graphics/Region.Op) have the ability to expand the clip. The canvas clipping APIs are intended to only expand the clip as a result of a restore operation. This enables a view parent to clip a canvas to clearly define the maximal drawing area of its children. The recommended alternative calls are [clipPath(android.graphics.Path)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#clipPath(android.graphics.Path))and [clipOutPath(android.graphics.Path)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#clipOutPath(android.graphics.Path)); As of API Level API level {@value android.os.Build.VERSION_CODES#P Build.VERSION_CODES.P} only [Region.Op.INTERSECT](https://developer.android.com/reference/kotlin/android/graphics/Region.Op) and [Region.Op.DIFFERENCE](https://developer.android.com/reference/kotlin/android/graphics/Region.Op) are valid Region.Op parameters.*

Modify the current clip with the specified path.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path):The path to operate on the current clip This value cannot be`null`. |
| `op` | [Region.Op](https://developer.android.com/reference/kotlin/android/graphics/Region.Op):How the clip is modified This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the resulting is non-empty |

### clipRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clipRect(rect: Rect): Boolean
```

Intersect the current clip with the specified rectangle, which is expressed in local coordinates.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rect` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect):The rectangle to intersect with the current clip. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the resulting clip is non-empty |

### clipRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clipRect(
    rect: Rect, 
    op: Region.Op
): Boolean
```

**Deprecated:** *Region.Op values other than [Region.Op.INTERSECT](https://developer.android.com/reference/kotlin/android/graphics/Region.Op) and [Region.Op.DIFFERENCE](https://developer.android.com/reference/kotlin/android/graphics/Region.Op) have the ability to expand the clip. The canvas clipping APIs are intended to only expand the clip as a result of a restore operation. This enables a view parent to clip a canvas to clearly define the maximal drawing area of its children. The recommended alternative calls are [clipRect(android.graphics.Rect)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#clipRect(android.graphics.Rect))and [clipOutRect(android.graphics.Rect)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#clipOutRect(android.graphics.Rect)); As of API Level API level {@value android.os.Build.VERSION_CODES#P Build.VERSION_CODES.P} only [Region.Op.INTERSECT](https://developer.android.com/reference/kotlin/android/graphics/Region.Op) and [Region.Op.DIFFERENCE](https://developer.android.com/reference/kotlin/android/graphics/Region.Op) are valid Region.Op parameters.*

Modify the current clip with the specified rectangle, which is expressed in local coordinates.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rect` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect):The rectangle to intersect with the current clip. This value cannot be`null`. |
| `op` | [Region.Op](https://developer.android.com/reference/kotlin/android/graphics/Region.Op):How the clip is modified This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the resulting clip is non-empty |

### clipRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clipRect(rect: RectF): Boolean
```

Intersect the current clip with the specified rectangle, which is expressed in local coordinates.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rect` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF):The rectangle to intersect with the current clip. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the resulting clip is non-empty |

### clipRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clipRect(
    rect: RectF, 
    op: Region.Op
): Boolean
```

**Deprecated:** *Region.Op values other than [Region.Op.INTERSECT](https://developer.android.com/reference/kotlin/android/graphics/Region.Op) and [Region.Op.DIFFERENCE](https://developer.android.com/reference/kotlin/android/graphics/Region.Op) have the ability to expand the clip. The canvas clipping APIs are intended to only expand the clip as a result of a restore operation. This enables a view parent to clip a canvas to clearly define the maximal drawing area of its children. The recommended alternative calls are [clipRect(android.graphics.RectF)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#clipRect(android.graphics.RectF))and [clipOutRect(android.graphics.RectF)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#clipOutRect(android.graphics.RectF)); As of API Level API level {@value android.os.Build.VERSION_CODES#P Build.VERSION_CODES.P} only [Region.Op.INTERSECT](https://developer.android.com/reference/kotlin/android/graphics/Region.Op) and [Region.Op.DIFFERENCE](https://developer.android.com/reference/kotlin/android/graphics/Region.Op) are valid Region.Op parameters.*

Modify the current clip with the specified rectangle.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rect` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF):The rect to intersect with the current clip This value cannot be`null`. |
| `op` | [Region.Op](https://developer.android.com/reference/kotlin/android/graphics/Region.Op):How the clip is modified This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the resulting clip is non-empty |

### clipRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clipRect(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float
): Boolean
```

Intersect the current clip with the specified rectangle, which is expressed in local coordinates.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `left` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The left side of the rectangle to intersect with the current clip |
| `top` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The top of the rectangle to intersect with the current clip |
| `right` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The right side of the rectangle to intersect with the current clip |
| `bottom` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The bottom of the rectangle to intersect with the current clip |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the resulting clip is non-empty |

### clipRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clipRect(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float, 
    op: Region.Op
): Boolean
```

**Deprecated:** *Region.Op values other than [Region.Op.INTERSECT](https://developer.android.com/reference/kotlin/android/graphics/Region.Op) and [Region.Op.DIFFERENCE](https://developer.android.com/reference/kotlin/android/graphics/Region.Op) have the ability to expand the clip. The canvas clipping APIs are intended to only expand the clip as a result of a restore operation. This enables a view parent to clip a canvas to clearly define the maximal drawing area of its children. The recommended alternative calls are [clipRect(float,float,float,float)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#clipRect(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))and [clipOutRect(float,float,float,float)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#clipOutRect(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float)); As of API Level API level {@value android.os.Build.VERSION_CODES#P Build.VERSION_CODES.P} only [Region.Op.INTERSECT](https://developer.android.com/reference/kotlin/android/graphics/Region.Op) and [Region.Op.DIFFERENCE](https://developer.android.com/reference/kotlin/android/graphics/Region.Op) are valid Region.Op parameters.*

Modify the current clip with the specified rectangle, which is expressed in local coordinates.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `left` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The left side of the rectangle to intersect with the current clip |
| `top` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The top of the rectangle to intersect with the current clip |
| `right` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The right side of the rectangle to intersect with the current clip |
| `bottom` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The bottom of the rectangle to intersect with the current clip |
| `op` | [Region.Op](https://developer.android.com/reference/kotlin/android/graphics/Region.Op):How the clip is modified This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the resulting clip is non-empty |

### clipRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clipRect(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Boolean
```

Intersect the current clip with the specified rectangle, which is expressed in local coordinates.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The left side of the rectangle to intersect with the current clip |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The top of the rectangle to intersect with the current clip |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The right side of the rectangle to intersect with the current clip |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The bottom of the rectangle to intersect with the current clip |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the resulting clip is non-empty |

### clipShader

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clipShader(shader: Shader): Unit
```

Intersect the current clip with the specified shader. The shader will be treated as an alpha mask, taking the intersection of the two.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `shader` | [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader):The shader to intersect with the current clip This value cannot be`null`. |

### concat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun concat(matrix: Matrix?): Unit
```

Preconcat the current matrix with the specified matrix. If the specified matrix is null, this method does nothing.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `matrix` | [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix)?:The matrix to preconcatenate with the current matrix This value may be`null`. |

### concat

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun concat(m: Matrix44?): Unit
```

Preconcat the current matrix with the specified matrix. If the specified matrix is null, this method does nothing. If the canvas's matrix is changed in the z-axis through this function, the deprecated [getMatrix()](https://developer.android.com/reference/kotlin/android/graphics/Canvas#getMatrix())method will return a 3x3 with z-axis info stripped away.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `m` | [Matrix44](https://developer.android.com/reference/kotlin/android/graphics/Matrix44)?:The 4x4 matrix to preconcatenate with the current matrix This value may be`null`. |

### disableZ

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun disableZ(): Unit
```

Disables Z support, preventing any RenderNodes drawn after this point from being visually reordered or having shadows rendered. Note: This is not impacted by any [save()](https://developer.android.com/reference/kotlin/android/graphics/Canvas#save())or [restore()](https://developer.android.com/reference/kotlin/android/graphics/Canvas#restore())calls as it is not considered to be part of the current matrix or clip. See [enableZ()](https://developer.android.com/reference/kotlin/android/graphics/Canvas#enableZ()) 

### drawARGB

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawARGB(
    a: Int, 
    r: Int, 
    g: Int, 
    b: Int
): Unit
```

Fill the entire canvas' bitmap (restricted to the current clip) with the specified ARGB color, using srcover porterduff mode.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------|
| `a` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):alpha component (0..255) of the color to draw onto the canvas |
| `r` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):red component (0..255) of the color to draw onto the canvas |
| `g` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):green component (0..255) of the color to draw onto the canvas |
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):blue component (0..255) of the color to draw onto the canvas |

### drawArc

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawArc(
    oval: RectF, 
    startAngle: Float, 
    sweepAngle: Float, 
    useCenter: Boolean, 
    paint: Paint
): Unit
```

Draw the specified arc, which will be scaled to fit inside the specified oval.

If the start angle is negative or \>= 360, the start angle is treated as start angle modulo 360.

If the sweep angle is \>= 360, then the oval is drawn completely. Note that this differs slightly from SkPath::arcTo, which treats the sweep angle modulo 360. If the sweep angle is negative, the sweep angle is treated as sweep angle modulo 360

The arc is drawn clockwise. An angle of 0 degrees correspond to the geometric angle of 0 degrees (3 o'clock on a watch.)

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `oval` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF):The bounds of oval used to define the shape and size of the arc This value cannot be`null`. |
| `startAngle` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Starting angle (in degrees) where the arc begins |
| `sweepAngle` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Sweep angle (in degrees) measured clockwise |
| `useCenter` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If true, include the center of the oval in the arc, and close it if it is being stroked. This will draw a wedge |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):The paint used to draw the arc This value cannot be`null`. |

### drawArc

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawArc(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float, 
    startAngle: Float, 
    sweepAngle: Float, 
    useCenter: Boolean, 
    paint: Paint
): Unit
```

Draw the specified arc, which will be scaled to fit inside the specified oval.

If the start angle is negative or \>= 360, the start angle is treated as start angle modulo 360.

If the sweep angle is \>= 360, then the oval is drawn completely. Note that this differs slightly from SkPath::arcTo, which treats the sweep angle modulo 360. If the sweep angle is negative, the sweep angle is treated as sweep angle modulo 360

The arc is drawn clockwise. An angle of 0 degrees correspond to the geometric angle of 0 degrees (3 o'clock on a watch.)

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `startAngle` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Starting angle (in degrees) where the arc begins |
| `sweepAngle` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Sweep angle (in degrees) measured clockwise |
| `useCenter` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If true, include the center of the oval in the arc, and close it if it is being stroked. This will draw a wedge |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):The paint used to draw the arc This value cannot be`null`. |

### drawBitmap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawBitmap(
    bitmap: Bitmap, 
    matrix: Matrix, 
    paint: Paint?
): Unit
```

Draw the bitmap using the specified matrix.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bitmap` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap):The bitmap to draw This value cannot be`null`. |
| `matrix` | [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix):The matrix used to transform the bitmap when it is drawn This value cannot be`null`. |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?:May be null. The paint used to draw the bitmap |

### drawBitmap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawBitmap(
    bitmap: Bitmap, 
    src: Rect?, 
    dst: Rect, 
    paint: Paint?
): Unit
```

Draw the specified bitmap, scaling/translating automatically to fill the destination rectangle. If the source rectangle is not null, it specifies the subset of the bitmap to draw.

Note: if the paint contains a maskfilter that generates a mask which extends beyond the bitmap's original width/height (e.g. BlurMaskFilter), then the bitmap will be drawn as if it were in a Shader with CLAMP mode. Thus the color outside of the original width/height will be the edge color replicated.

This function*ignores the density associated with the bitmap*. This is because the source and destination rectangle coordinate spaces are in their respective densities, so must already have the appropriate scaling factor applied.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bitmap` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap):The bitmap to be drawn This value cannot be`null`. |
| `src` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect)?:May be null. The subset of the bitmap to be drawn |
| `dst` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect):The rectangle that the bitmap will be scaled/translated to fit into This value cannot be`null`. |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?:May be null. The paint used to draw the bitmap |

### drawBitmap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawBitmap(
    bitmap: Bitmap, 
    src: Rect?, 
    dst: RectF, 
    paint: Paint?
): Unit
```

Draw the specified bitmap, scaling/translating automatically to fill the destination rectangle. If the source rectangle is not null, it specifies the subset of the bitmap to draw.

Note: if the paint contains a maskfilter that generates a mask which extends beyond the bitmap's original width/height (e.g. BlurMaskFilter), then the bitmap will be drawn as if it were in a Shader with CLAMP mode. Thus the color outside of the original width/height will be the edge color replicated.

This function*ignores the density associated with the bitmap*. This is because the source and destination rectangle coordinate spaces are in their respective densities, so must already have the appropriate scaling factor applied.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bitmap` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap):The bitmap to be drawn This value cannot be`null`. |
| `src` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect)?:May be null. The subset of the bitmap to be drawn |
| `dst` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF):The rectangle that the bitmap will be scaled/translated to fit into This value cannot be`null`. |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?:May be null. The paint used to draw the bitmap |

### drawBitmap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawBitmap(
    bitmap: Bitmap, 
    left: Float, 
    top: Float, 
    paint: Paint?
): Unit
```

Draw the specified bitmap, with its top/left corner at (x,y), using the specified paint, transformed by the current matrix.

Note: if the paint contains a maskfilter that generates a mask which extends beyond the bitmap's original width/height (e.g. BlurMaskFilter), then the bitmap will be drawn as if it were in a Shader with CLAMP mode. Thus the color outside of the original width/height will be the edge color replicated.

If the bitmap and canvas have different densities, this function will take care of automatically scaling the bitmap to draw at the same density as the canvas.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `bitmap` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap):The bitmap to be drawn This value cannot be`null`. |
| `left` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The position of the left side of the bitmap being drawn |
| `top` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The position of the top side of the bitmap being drawn |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?:The paint used to draw the bitmap (may be null) |

### drawBitmap

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawBitmap(
    colors: IntArray, 
    offset: Int, 
    stride: Int, 
    x: Float, 
    y: Float, 
    width: Int, 
    height: Int, 
    hasAlpha: Boolean, 
    paint: Paint?
): Unit
```

**Deprecated:** *Usage with a [hardware accelerated](https://developer.android.com/reference/kotlin/android/graphics/Canvas#isHardwareAccelerated())canvas requires an internal copy of color buffer contents every time this method is called. Using a Bitmap avoids this copy, and allows the application to more explicitly control the lifetime and copies of pixel data.*

Treat the specified array of colors as a bitmap, and draw it. This gives the same result as first creating a bitmap from the array, and then drawing it, but this method avoids explicitly creating a bitmap object which can be more efficient if the colors are changing often.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `colors` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html):Array of colors representing the pixels of the bitmap This value cannot be`null`. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset into the array of colors for the first pixel |
| `stride` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of colors in the array between rows (must be \>= width or \<= -width). |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The X coordinate for where to draw the bitmap |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The Y coordinate for where to draw the bitmap |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The width of the bitmap |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The height of the bitmap |
| `hasAlpha` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the alpha channel of the colors contains valid values. If false, the alpha byte is ignored (assumed to be 0xFF for every pixel). |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?:May be null. The paint used to draw the bitmap |

### drawBitmap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawBitmap(
    colors: IntArray, 
    offset: Int, 
    stride: Int, 
    x: Int, 
    y: Int, 
    width: Int, 
    height: Int, 
    hasAlpha: Boolean, 
    paint: Paint?
): Unit
```

**Deprecated:** *Usage with a [hardware accelerated](https://developer.android.com/reference/kotlin/android/graphics/Canvas#isHardwareAccelerated())canvas requires an internal copy of color buffer contents every time this method is called. Using a Bitmap avoids this copy, and allows the application to more explicitly control the lifetime and copies of pixel data.*

Legacy version of drawBitmap(int\[\] colors, ...) that took ints for x,y

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------|
| `colors` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html):This value cannot be`null`. |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?:This value may be`null`. |

### drawBitmapMesh

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawBitmapMesh(
    bitmap: Bitmap, 
    meshWidth: Int, 
    meshHeight: Int, 
    verts: FloatArray, 
    vertOffset: Int, 
    colors: IntArray?, 
    colorOffset: Int, 
    paint: Paint?
): Unit
```

Draw the bitmap through the mesh, where mesh vertices are evenly distributed across the bitmap. There are meshWidth+1 vertices across, and meshHeight+1 vertices down. The verts array is accessed in row-major order, so that the first meshWidth+1 vertices are distributed across the top of the bitmap from left to right. A more general version of this method is drawVertices(). Prior to API level {@value android.os.Build.VERSION_CODES#P Build.VERSION_CODES.P} vertOffset and colorOffset were ignored, effectively treating them as zeros. In API level {@value android.os.Build.VERSION_CODES#P Build.VERSION_CODES.P} and above these parameters will be respected.

Note: antialiasing is not supported, therefore [Paint.ANTI_ALIAS_FLAG](https://developer.android.com/reference/kotlin/android/graphics/Paint#ANTI_ALIAS_FLAG:kotlin.Int) is ignored.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bitmap` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap):The bitmap to draw using the mesh This value cannot be`null`. |
| `meshWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of columns in the mesh. Nothing is drawn if this is 0 |
| `meshHeight` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of rows in the mesh. Nothing is drawn if this is 0 |
| `verts` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html):Array of x,y pairs, specifying where the mesh should be drawn. There must be at least (meshWidth+1) \* (meshHeight+1) \* 2 + vertOffset values in the array This value cannot be`null`. |
| `vertOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of verts elements to skip before drawing |
| `colors` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?:May be null. Specifies a color at each vertex, which is interpolated across the cell, and whose values are multiplied by the corresponding bitmap colors. If not null, there must be at least (meshWidth+1) \* (meshHeight+1) + colorOffset values in the array. |
| `colorOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of color elements to skip before drawing |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?:May be null. The paint used to draw the bitmap. Antialiasing is not supported. |

### drawCircle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawCircle(
    cx: Float, 
    cy: Float, 
    radius: Float, 
    paint: Paint
): Unit
```

Draw the specified circle using the specified paint. If radius is \<= 0, then nothing will be drawn. The circle will be filled or framed based on the Style in the paint.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `cx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-coordinate of the center of the circle to be drawn |
| `cy` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-coordinate of the center of the circle to be drawn |
| `radius` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The radius of the circle to be drawn |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):The paint used to draw the circle This value cannot be`null`. |

### drawColor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawColor(color: Int): Unit
```

Fill the entire canvas' bitmap (restricted to the current clip) with the specified color, using srcover porterduff mode.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the color to draw onto the canvas |

### drawColor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawColor(
    color: Int, 
    mode: BlendMode
): Unit
```

Fill the entire canvas' bitmap (restricted to the current clip) with the specified color and blendmode.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the color to draw onto the canvas |
| `mode` | [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode):the blendmode to apply to the color This value cannot be`null`. |

### drawColor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawColor(
    color: Int, 
    mode: PorterDuff.Mode
): Unit
```

Fill the entire canvas' bitmap (restricted to the current clip) with the specified color and porter-duff xfermode.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the color to draw onto the canvas |
| `mode` | [PorterDuff.Mode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode):the porter-duff mode to apply to the color This value cannot be`null`. |

### drawColor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawColor(color: Long): Unit
```

Fill the entire canvas' bitmap (restricted to the current clip) with the specified color, using srcover porterduff mode.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `color` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the`ColorLong`to draw onto the canvas. See the [Color](https://developer.android.com/reference/kotlin/android/graphics/Color) class for details about`ColorLong`s. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the color space encoded in the`ColorLong`is invalid or unknown. |

### drawColor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawColor(
    color: Long, 
    mode: BlendMode
): Unit
```

Fill the entire canvas' bitmap (restricted to the current clip) with the specified color and blendmode.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `color` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the`ColorLong`to draw onto the canvas. See the [Color](https://developer.android.com/reference/kotlin/android/graphics/Color) class for details about`ColorLong`s. |
| `mode` | [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode):the blendmode to apply to the color This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the color space encoded in the`ColorLong`is invalid or unknown. |

### drawDoubleRoundRect

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawDoubleRoundRect(
    outer: RectF, 
    outerRx: Float, 
    outerRy: Float, 
    inner: RectF, 
    innerRx: Float, 
    innerRy: Float, 
    paint: Paint
): Unit
```

Draws a double rounded rectangle using the specified paint. The resultant round rect will be filled in the area defined between the outer and inner rectangular bounds if the [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint) configured with [Paint.Style.FILL](https://developer.android.com/reference/kotlin/android/graphics/Paint.Style). Otherwise if [Paint.Style.STROKE](https://developer.android.com/reference/kotlin/android/graphics/Paint.Style) is used, then 2 rounded rect strokes will be drawn at the outer and inner rounded rectangles

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `outer` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF):The outer rectangular bounds of the roundRect to be drawn This value cannot be`null`. |
| `outerRx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-radius of the oval used to round the corners on the outer rectangle |
| `outerRy` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-radius of the oval used to round the corners on the outer rectangle |
| `inner` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF):The inner rectangular bounds of the roundRect to be drawn This value cannot be`null`. |
| `innerRx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-radius of the oval used to round the corners on the inner rectangle |
| `innerRy` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-radius of the oval used to round the corners on the outer rectangle |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):The paint used to draw the double roundRect This value cannot be`null`. |

### drawDoubleRoundRect

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawDoubleRoundRect(
    outer: RectF, 
    outerRadii: FloatArray, 
    inner: RectF, 
    innerRadii: FloatArray, 
    paint: Paint
): Unit
```

Draws a double rounded rectangle using the specified paint. The resultant round rect will be filled in the area defined between the outer and inner rectangular bounds if the [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint) configured with [Paint.Style.FILL](https://developer.android.com/reference/kotlin/android/graphics/Paint.Style). Otherwise if [Paint.Style.STROKE](https://developer.android.com/reference/kotlin/android/graphics/Paint.Style) is used, then 2 rounded rect strokes will be drawn at the outer and inner rounded rectangles

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `outer` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF):The outer rectangular bounds of the roundRect to be drawn This value cannot be`null`. |
| `outerRadii` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html):Array of 8 float representing the x, y corner radii for top left, top right, bottom right, bottom left corners respectively on the outer rounded rectangle This value cannot be`null`. |
| `inner` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF):The inner rectangular bounds of the roundRect to be drawn This value cannot be`null`. |
| `innerRadii` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html):Array of 8 float representing the x, y corner radii for top left, top right, bottom right, bottom left corners respectively on the outer rounded rectangle This value cannot be`null`. |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):The paint used to draw the double roundRect This value cannot be`null`. |

### drawGlyphs

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawGlyphs(
    glyphIds: IntArray, 
    glyphIdOffset: Int, 
    positions: FloatArray, 
    positionOffset: Int, 
    glyphCount: Int, 
    font: Font, 
    paint: Paint
): Unit
```

Draw array of glyphs with specified font.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `glyphIds` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html):Array of glyph IDs. The length of array must be greater than or equal to`glyphIdOffset + glyphCount`. This value cannot be`null`. |
| `glyphIdOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of elements to skip before drawing in`glyphIds`array. Value is 0 or greater |
| `positions` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html):A flattened X and Y position array. The first glyph X position must be stored at`positionOffset`. The first glyph Y position must be stored at`positionOffset + 1`, then the second glyph X position must be stored at`positionOffset + 2`. The length of array must be greater than or equal to`positionOffset + glyphCount * 2`. This value cannot be`null`. |
| `positionOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of elements to skip before drawing in`positions`. The first glyph X position must be stored at`positionOffset`. The first glyph Y position must be stored at`positionOffset + 1`, then the second glyph X position must be stored at`positionOffset + 2`. Value is 0 or greater |
| `glyphCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of glyphs to be drawn. Value is 0 or greater |
| `font` | [Font](https://developer.android.com/reference/kotlin/android/graphics/fonts/Font):Font used for drawing. This value cannot be`null`. |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):Paint used for drawing. The typeface set to this paint is ignored. This value cannot be`null`. |

**See Also**

- [android.graphics.text.TextRunShaper](https://developer.android.com/reference/kotlin/android/graphics/text/TextRunShaper)
- [android.text.TextShaper](https://developer.android.com/reference/kotlin/android/text/TextShaper.html#) 

### drawLine

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawLine(
    startX: Float, 
    startY: Float, 
    stopX: Float, 
    stopY: Float, 
    paint: Paint
): Unit
```

Draw a line segment with the specified start and stop x,y coordinates, using the specified paint.

Note that since a line is always "framed", the Style is ignored in the paint.

Degenerate lines (length is 0) will not be drawn.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `startX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-coordinate of the start point of the line |
| `startY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-coordinate of the start point of the line |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):The paint used to draw the line This value cannot be`null`. |

### drawLines

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawLines(
    pts: FloatArray, 
    paint: Paint
): Unit
```

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------|
| `pts` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html):This value cannot be`null`. |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):This value cannot be`null`. |

### drawLines

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawLines(
    pts: FloatArray, 
    offset: Int, 
    count: Int, 
    paint: Paint
): Unit
```

Draw a series of lines. Each line is taken from 4 consecutive values in the pts array. Thus to draw 1 line, the array must contain at least 4 values. This is logically the same as drawing the array as follows: drawLine(pts\[0\], pts\[1\], pts\[2\], pts\[3\]) followed by drawLine(pts\[4\], pts\[5\], pts\[6\], pts\[7\]) and so on.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pts` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html):Array of points to draw \[x0 y0 x1 y1 x2 y2 ...\] This value cannot be`null`. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of values in the array to skip before drawing. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of values in the array to process, after skipping "offset" of them. Since each line uses 4 values, the number of "lines" that are drawn is really (count \>\> 2). |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):The paint used to draw the points This value cannot be`null`. |

### drawMesh

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawMesh(
    mesh: Mesh, 
    blendMode: BlendMode?, 
    paint: Paint
): Unit
```

Draws a mesh object to the screen.

Note: antialiasing is not supported, therefore [Paint.ANTI_ALIAS_FLAG](https://developer.android.com/reference/kotlin/android/graphics/Paint#ANTI_ALIAS_FLAG:kotlin.Int) is ignored.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mesh` | [Mesh](https://developer.android.com/reference/kotlin/android/graphics/Mesh): [Mesh](https://developer.android.com/reference/kotlin/android/graphics/Mesh) object that will be drawn to the screen This value cannot be`null`. |
| `blendMode` | [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode)?: [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode) used to blend mesh primitives as the destination color with the Paint color/shader as the source color. This defaults to [BlendMode.MODULATE](https://developer.android.com/reference/kotlin/android/graphics/BlendMode) if null. |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint): [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint) used to provide a color/shader/blend mode. This value cannot be`null`. |

### drawOval

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawOval(
    oval: RectF, 
    paint: Paint
): Unit
```

Draw the specified oval using the specified paint. The oval will be filled or framed based on the Style in the paint.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `oval` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF):The rectangle bounds of the oval to be drawn This value cannot be`null`. |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):This value cannot be`null`. |

### drawOval

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawOval(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float, 
    paint: Paint
): Unit
```

Draw the specified oval using the specified paint. The oval will be filled or framed based on the Style in the paint.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------|
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):This value cannot be`null`. |

### drawPaint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawPaint(paint: Paint): Unit
```

Fill the entire canvas' bitmap (restricted to the current clip) with the specified paint. This is equivalent (but faster) to drawing an infinitely large rectangle with the specified paint.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):The paint used to draw onto the canvas This value cannot be`null`. |

### drawPatch

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawPatch(
    patch: NinePatch, 
    dst: Rect, 
    paint: Paint?
): Unit
```

Draws the specified bitmap as an N-patch (most often, a 9-patch.)

Note: antialiasing is not supported, therefore [Paint.ANTI_ALIAS_FLAG](https://developer.android.com/reference/kotlin/android/graphics/Paint#ANTI_ALIAS_FLAG:kotlin.Int) is ignored.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `patch` | [NinePatch](https://developer.android.com/reference/kotlin/android/graphics/NinePatch):The ninepatch object to render This value cannot be`null`. |
| `dst` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect):The destination rectangle. This value cannot be`null`. |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?:The paint to draw the bitmap with. May be null. Antialiasing is not supported. |

### drawPatch

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawPatch(
    patch: NinePatch, 
    dst: RectF, 
    paint: Paint?
): Unit
```

Draws the specified bitmap as an N-patch (most often, a 9-patch.)

Note: antialiasing is not supported, therefore [Paint.ANTI_ALIAS_FLAG](https://developer.android.com/reference/kotlin/android/graphics/Paint#ANTI_ALIAS_FLAG:kotlin.Int) is ignored.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `patch` | [NinePatch](https://developer.android.com/reference/kotlin/android/graphics/NinePatch):The ninepatch object to render This value cannot be`null`. |
| `dst` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF):The destination rectangle. This value cannot be`null`. |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?:The paint to draw the bitmap with. May be null. Antialiasing is not supported. |

### drawPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawPath(
    path: Path, 
    paint: Paint
): Unit
```

Draw the specified path using the specified paint. The path will be filled or framed based on the Style in the paint.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path):The path to be drawn This value cannot be`null`. |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):The paint used to draw the path This value cannot be`null`. |

### drawPicture

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawPicture(picture: Picture): Unit
```

Save the canvas state, draw the picture, and restore the canvas state. This differs from picture.draw(canvas), which does not perform any save/restore.

**Note:** This forces the picture to internally call [Picture.endRecording](https://developer.android.com/reference/kotlin/android/graphics/Picture#endRecording())in order to prepare for playback.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `picture` | [Picture](https://developer.android.com/reference/kotlin/android/graphics/Picture):The picture to be drawn This value cannot be`null`. |

### drawPicture

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawPicture(
    picture: Picture, 
    dst: Rect
): Unit
```

Draw the picture, stretched to fit into the dst rectangle.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------|
| `picture` | [Picture](https://developer.android.com/reference/kotlin/android/graphics/Picture):This value cannot be`null`. |
| `dst` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect):This value cannot be`null`. |

### drawPicture

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawPicture(
    picture: Picture, 
    dst: RectF
): Unit
```

Draw the picture, stretched to fit into the dst rectangle.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------|
| `picture` | [Picture](https://developer.android.com/reference/kotlin/android/graphics/Picture):This value cannot be`null`. |
| `dst` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF):This value cannot be`null`. |

### drawPoint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawPoint(
    x: Float, 
    y: Float, 
    paint: Paint
): Unit
```

Helper for drawPoints() for drawing a single point.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------|
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):This value cannot be`null`. |

### drawPoints

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawPoints(
    pts: FloatArray, 
    paint: Paint
): Unit
```

Helper for drawPoints() that assumes you want to draw the entire array

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------|
| `pts` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html):This value cannot be`null`. |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):This value cannot be`null`. |

### drawPoints

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawPoints(
    pts: FloatArray!, 
    offset: Int, 
    count: Int, 
    paint: Paint
): Unit
```

Draw a series of points. Each point is centered at the coordinate specified by pts\[\], and its diameter is specified by the paint's stroke width (as transformed by the canvas' CTM), with special treatment for a stroke width of 0, which always draws exactly 1 pixel (or at most 4 if antialiasing is enabled). The shape of the point is controlled by the paint's Cap type. The shape is a square, unless the cap type is Round, in which case the shape is a circle.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pts` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:Array of points to draw \[x0 y0 x1 y1 x2 y2 ...\] |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of values to skip before starting to draw. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of values to process, after skipping offset of them. Since one point uses two values, the number of "points" that are drawn is really (count \>\> 1). |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):The paint used to draw the points This value cannot be`null`. |

### drawPosText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawPosText(
    text: CharArray, 
    index: Int, 
    count: Int, 
    pos: FloatArray, 
    paint: Paint
): Unit
```

**Deprecated:** *This method does not support glyph composition and decomposition and should therefore not be used to render complex scripts. It also doesn't handle supplementary characters (eg emoji).*

Draw the text in the array, with each character's origin specified by the pos array.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html):The text to be drawn This value cannot be`null`. |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the first character to draw |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of characters to draw, starting from index. |
| `pos` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html):Array of \[x,y\] positions, used to position each character This value cannot be`null`. |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):The paint used for the text (e.g. color, size, style) This value cannot be`null`. |

### drawPosText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawPosText(
    text: String, 
    pos: FloatArray, 
    paint: Paint
): Unit
```

**Deprecated:** *This method does not support glyph composition and decomposition and should therefore not be used to render complex scripts. It also doesn't handle supplementary characters (eg emoji).*

Draw the text in the array, with each character's origin specified by the pos array.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The text to be drawn This value cannot be`null`. |
| `pos` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html):Array of \[x,y\] positions, used to position each character This value cannot be`null`. |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):The paint used for the text (e.g. color, size, style) This value cannot be`null`. |

### drawRGB

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawRGB(
    r: Int, 
    g: Int, 
    b: Int
): Unit
```

Fill the entire canvas' bitmap (restricted to the current clip) with the specified RGB color, using srcover porterduff mode.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):red component (0..255) of the color to draw onto the canvas |
| `g` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):green component (0..255) of the color to draw onto the canvas |
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):blue component (0..255) of the color to draw onto the canvas |

### drawRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawRect(
    r: Rect, 
    paint: Paint
): Unit
```

Draw the specified Rect using the specified Paint. The rectangle will be filled or framed based on the Style in the paint.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect):The rectangle to be drawn. This value cannot be`null`. |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):The paint used to draw the rectangle This value cannot be`null`. |

### drawRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawRect(
    rect: RectF, 
    paint: Paint
): Unit
```

Draw the specified Rect using the specified paint. The rectangle will be filled or framed based on the Style in the paint.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `rect` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF):The rect to be drawn This value cannot be`null`. |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):The paint used to draw the rect This value cannot be`null`. |

### drawRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawRect(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float, 
    paint: Paint
): Unit
```

Draw the specified Rect using the specified paint. The rectangle will be filled or framed based on the Style in the paint.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `left` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The left side of the rectangle to be drawn |
| `top` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The top side of the rectangle to be drawn |
| `right` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The right side of the rectangle to be drawn |
| `bottom` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The bottom side of the rectangle to be drawn |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):The paint used to draw the rect This value cannot be`null`. |

### drawRegion

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawRegion(
    region: Region, 
    paint: Paint
): Unit
```

Draws the given region using the given paint.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `region` | [Region](https://developer.android.com/reference/kotlin/android/graphics/Region):The region to be drawn This value cannot be`null`. |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):The paint used to draw the region This value cannot be`null`. |

### drawRenderNode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawRenderNode(renderNode: RenderNode): Unit
```

Draws the given RenderNode. This is only supported in hardware rendering, which can be verified by asserting that [isHardwareAccelerated()](https://developer.android.com/reference/kotlin/android/graphics/Canvas#isHardwareAccelerated())is true. If [isHardwareAccelerated()](https://developer.android.com/reference/kotlin/android/graphics/Canvas#isHardwareAccelerated())is false then this throws an exception. See [RenderNode](https://developer.android.com/reference/kotlin/android/graphics/RenderNode) for more information on what a RenderNode is and how to use it.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------|
| `renderNode` | [RenderNode](https://developer.android.com/reference/kotlin/android/graphics/RenderNode):The RenderNode to draw, must be non-null. |

### drawRoundRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawRoundRect(
    rect: RectF, 
    rx: Float, 
    ry: Float, 
    paint: Paint
): Unit
```

Draw the specified round-rect using the specified paint. The roundrect will be filled or framed based on the Style in the paint.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rect` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF):The rectangular bounds of the roundRect to be drawn This value cannot be`null`. |
| `rx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-radius of the oval used to round the corners |
| `ry` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-radius of the oval used to round the corners |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):The paint used to draw the roundRect This value cannot be`null`. |

### drawRoundRect

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawRoundRect(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float, 
    rx: Float, 
    ry: Float, 
    paint: Paint
): Unit
```

Draw the specified round-rect using the specified paint. The roundrect will be filled or framed based on the Style in the paint.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `rx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-radius of the oval used to round the corners |
| `ry` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-radius of the oval used to round the corners |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):The paint used to draw the roundRect This value cannot be`null`. |

### drawText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawText(
    text: CharArray, 
    index: Int, 
    count: Int, 
    x: Float, 
    y: Float, 
    paint: Paint
): Unit
```

Draw the text, with origin at (x,y), using the specified paint. The origin is interpreted based on the Align setting in the paint.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html):The text to be drawn This value cannot be`null`. |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-coordinate of the origin of the text being drawn |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-coordinate of the baseline of the text being drawn |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):The paint used for the text (e.g. color, size, style) This value cannot be`null`. |

### drawText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawText(
    text: CharSequence, 
    start: Int, 
    end: Int, 
    x: Float, 
    y: Float, 
    paint: Paint
): Unit
```

Draw the specified range of text, specified by start/end, with its origin at (x,y), in the specified Paint. The origin is interpreted based on the Align setting in the Paint.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):The text to be drawn This value cannot be`null`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the first character in text to draw |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):(end - 1) is the index of the last character in text to draw |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-coordinate of origin for where to draw the text |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-coordinate of origin for where to draw the text |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):The paint used for the text (e.g. color, size, style) This value cannot be`null`. |

### drawText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawText(
    text: String, 
    x: Float, 
    y: Float, 
    paint: Paint
): Unit
```

Draw the text, with origin at (x,y), using the specified paint. The origin is interpreted based on the Align setting in the paint.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The text to be drawn This value cannot be`null`. |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-coordinate of the origin of the text being drawn |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-coordinate of the baseline of the text being drawn |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):The paint used for the text (e.g. color, size, style) This value cannot be`null`. |

### drawText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawText(
    text: String, 
    start: Int, 
    end: Int, 
    x: Float, 
    y: Float, 
    paint: Paint
): Unit
```

Draw the text, with origin at (x,y), using the specified paint. The origin is interpreted based on the Align setting in the paint.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The text to be drawn This value cannot be`null`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the first character in text to draw |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):(end - 1) is the index of the last character in text to draw |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-coordinate of the origin of the text being drawn |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-coordinate of the baseline of the text being drawn |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):The paint used for the text (e.g. color, size, style) This value cannot be`null`. |

### drawTextOnPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawTextOnPath(
    text: CharArray, 
    index: Int, 
    count: Int, 
    path: Path, 
    hOffset: Float, 
    vOffset: Float, 
    paint: Paint
): Unit
```

Draw the text, with origin at (x,y), using the specified paint, along the specified path. The paint's Align setting determines where along the path to start the text.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html):The text to be drawn This value cannot be`null`. |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The starting index within the text to be drawn |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Starting from index, the number of characters to draw |
| `path` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path):The path the text should follow for its baseline This value cannot be`null`. |
| `hOffset` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The distance along the path to add to the text's starting position |
| `vOffset` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The distance above(-) or below(+) the path to position the text |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):The paint used for the text (e.g. color, size, style) This value cannot be`null`. |

### drawTextOnPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawTextOnPath(
    text: String, 
    path: Path, 
    hOffset: Float, 
    vOffset: Float, 
    paint: Paint
): Unit
```

Draw the text, with origin at (x,y), using the specified paint, along the specified path. The paint's Align setting determines where along the path to start the text.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The text to be drawn This value cannot be`null`. |
| `path` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path):The path the text should follow for its baseline This value cannot be`null`. |
| `hOffset` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The distance along the path to add to the text's starting position |
| `vOffset` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The distance above(-) or below(+) the path to position the text |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):The paint used for the text (e.g. color, size, style) This value cannot be`null`. |

### drawTextRun

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawTextRun(
    text: MeasuredText, 
    start: Int, 
    end: Int, 
    contextStart: Int, 
    contextEnd: Int, 
    x: Float, 
    y: Float, 
    isRtl: Boolean, 
    paint: Paint
): Unit
```

Draw a run of text, all in a single direction, with optional context for complex text shaping.

See [drawTextRun(java.lang.CharSequence,int,int,int,int,float,float,boolean,android.graphics.Paint)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawTextRun(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20kotlin.Boolean,%20android.graphics.Paint))for more details. This method uses a [MeasuredText](https://developer.android.com/reference/kotlin/android/graphics/text/MeasuredText) rather than CharSequence to represent the string.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [MeasuredText](https://developer.android.com/reference/kotlin/android/graphics/text/MeasuredText):the text to render This value cannot be`null`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start of the text to render. Data before this position can be used for shaping context. |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the end of the text to render. Data at or after this position can be used for shaping context. |
| `contextStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the start of the shaping context |
| `contextEnd` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the end of the shaping context |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the x position at which to draw the text |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the y position at which to draw the text |
| `isRtl` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether the run is in RTL direction |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):the paint This value cannot be`null`. |

### drawTextRun

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawTextRun(
    text: CharArray, 
    index: Int, 
    count: Int, 
    contextIndex: Int, 
    contextCount: Int, 
    x: Float, 
    y: Float, 
    isRtl: Boolean, 
    paint: Paint
): Unit
```

Draw a run of text, all in a single direction, with optional context for complex text shaping.

See [drawTextRun(java.lang.CharSequence,int,int,int,int,float,float,boolean,android.graphics.Paint)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawTextRun(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20kotlin.Boolean,%20android.graphics.Paint))for more details. This method uses a character array rather than CharSequence to represent the string. Also, to be consistent with the pattern established in #drawText, in this method`count`and`contextCount`are used rather than offsets of the end position;`count = end - start, contextCount = contextEnd - contextStart`.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html):the text to render This value cannot be`null`. |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start of the text to render |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the count of chars to render |
| `contextIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start of the context for shaping. Must be no greater than index. |
| `contextCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of characters in the context for shaping. contexIndex + contextCount must be no less than index + count. |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the x position at which to draw the text |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the y position at which to draw the text |
| `isRtl` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether the run is in RTL direction |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):the paint This value cannot be`null`. |

### drawTextRun

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawTextRun(
    text: CharSequence, 
    start: Int, 
    end: Int, 
    contextStart: Int, 
    contextEnd: Int, 
    x: Float, 
    y: Float, 
    isRtl: Boolean, 
    paint: Paint
): Unit
```

Draw a run of text, all in a single direction, with optional context for complex text shaping.

The run of text includes the characters from`start`to`end`in the text. In addition, the range`contextStart`to`contextEnd`is used as context for the purpose of complex text shaping, such as Arabic text potentially shaped differently based on the text next to it.

All text outside the range`contextStart..contextEnd`is ignored. The text between`start`and`end`will be laid out and drawn. The context range is useful for contextual shaping, e.g. Kerning, Arabic contextural form.

The direction of the run is explicitly specified by`isRtl`. Thus, this method is suitable only for runs of a single direction. Alignment of the text is as determined by the Paint's TextAlign value. Further,`0 <= contextStart <= start <= end <= contextEnd <= text.length`must hold on entry.

Also see android.graphics.Paint#getRunAdvance for a corresponding method to measure the text; the advance width of the text drawn matches the value obtained from that method.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):the text to render This value cannot be`null`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start of the text to render. Data before this position can be used for shaping context. |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the end of the text to render. Data at or after this position can be used for shaping context. |
| `contextStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the start of the shaping context |
| `contextEnd` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the end of the shaping context |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the x position at which to draw the text |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the y position at which to draw the text |
| `isRtl` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether the run is in RTL direction |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):the paint This value cannot be`null`. |

**See Also**

- [#drawTextRun(char[], int, int, int, int, float, float, boolean, Paint)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawTextRun(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20kotlin.Boolean,%20android.graphics.Paint)) 

### drawVertices

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawVertices(
    mode: Canvas.VertexMode, 
    vertexCount: Int, 
    verts: FloatArray, 
    vertOffset: Int, 
    texs: FloatArray?, 
    texOffset: Int, 
    colors: IntArray?, 
    colorOffset: Int, 
    indices: ShortArray?, 
    indexOffset: Int, 
    indexCount: Int, 
    paint: Paint
): Unit
```

Draw the array of vertices, interpreted as triangles (based on mode). The verts array is required, and specifies the x,y pairs for each vertex. If texs is non-null, then it is used to specify the coordinate in shader coordinates to use at each vertex (the paint must have a shader in this case). If there is no texs array, but there is a color array, then each color is interpolated across its corresponding triangle in a gradient. If both texs and colors arrays are present, then they behave as before, but the resulting color at each pixels is the result of multiplying the colors from the shader and the color-gradient together. The indices array is optional, but if it is present, then it is used to specify the index of each triangle, rather than just walking through the arrays in order.

Note: antialiasing is not supported, therefore [Paint.ANTI_ALIAS_FLAG](https://developer.android.com/reference/kotlin/android/graphics/Paint#ANTI_ALIAS_FLAG:kotlin.Int) is ignored.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [Canvas.VertexMode](https://developer.android.com/reference/kotlin/android/graphics/Canvas.VertexMode):How to interpret the array of vertices This value cannot be`null`. |
| `vertexCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of values in the vertices array (and corresponding texs and colors arrays if non-null). Each logical vertex is two values (x, y), vertexCount must be a multiple of 2. |
| `verts` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html):Array of vertices for the mesh This value cannot be`null`. |
| `vertOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of values in the verts to skip before drawing. |
| `texs` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?:May be null. If not null, specifies the coordinates to sample into the current shader (e.g. bitmap tile or gradient) |
| `texOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of values in texs to skip before drawing. |
| `colors` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?:May be null. If not null, specifies a color for each vertex, to be interpolated across the triangle. |
| `colorOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of values in colors to skip before drawing. |
| `indices` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)?:If not null, array of indices to reference into the vertex (texs, colors) array. |
| `indexCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of entries in the indices array (if not null). |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint):Specifies the shader to use if the texs array is non-null. Antialiasing is not supported. |

### enableZ

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun enableZ(): Unit
```

Enables Z support which defaults to disabled. This allows for RenderNodes drawn with [drawRenderNode(android.graphics.RenderNode)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawRenderNode(android.graphics.RenderNode))to be re-arranged based off of their [RenderNode.getElevation()](https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getElevation())and [RenderNode.getTranslationZ()](https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getTranslationZ())values. It also enables rendering of shadows for RenderNodes with an elevation or translationZ.

Any draw reordering will not be moved before this call. A typical usage of this might look something like: 

```kotlin
void draw(Canvas canvas) {
          // Draw any background content
          canvas.drawColor(backgroundColor);
 
          // Begin drawing that may be reordered based off of Z
          canvas.enableZ();
          for (RenderNode child : children) {
              canvas.drawRenderNode(child);
          }
          // End drawing that may be reordered based off of Z
          canvas.disableZ();
 
          // Draw any overlays
          canvas.drawText("I'm on top of everything!", 0, 0, paint);
      }
  
```

<br />

Note: This is not impacted by any [save()](https://developer.android.com/reference/kotlin/android/graphics/Canvas#save())or [restore()](https://developer.android.com/reference/kotlin/android/graphics/Canvas#restore())calls as it is not considered to be part of the current matrix or clip. See [disableZ()](https://developer.android.com/reference/kotlin/android/graphics/Canvas#disableZ()) 

### getClipBounds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClipBounds(): Rect
```

Retrieve the bounds of the current clip (in local coordinates).

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect) | the clip bounds, or \[0, 0, 0, 0\] if the clip is empty. This value cannot be`null`. |

### getClipBounds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getClipBounds(bounds: Rect): Boolean
```

Return the bounds of the current clip (in local coordinates) in the bounds parameter, and return true if it is non-empty. This can be useful in a way similar to quickReject, in that it tells you that drawing outside of these bounds will be clipped out.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| `bounds` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect):Return the clip bounds here. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the current clip is non-empty. |

### getDensity

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDensity(): Int
```

Returns the target density of the canvas. The default density is derived from the density of its backing bitmap, or [Bitmap.DENSITY_NONE](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#DENSITY_NONE:kotlin.Int) if there is not one.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Returns the current target density of the canvas, which is used to determine the scaling factor when drawing a bitmap into it. |

**See Also**

- [#setDensity(int)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#setDensity(kotlin.Int))
- [android.graphics.Bitmap#getDensity()](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getDensity()) 

### getDrawFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDrawFilter(): DrawFilter?
```

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------|
| [DrawFilter](https://developer.android.com/reference/kotlin/android/graphics/DrawFilter)? | This value may be`null`. |

### getHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHeight(): Int
```

Returns the height of the current drawing layer

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the height of the current drawing layer |

### getMatrix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMatrix(): Matrix
```

**Deprecated:** * [Hardware accelerated](https://developer.android.com/reference/kotlin/android/graphics/Canvas#isHardwareAccelerated())canvases may have any matrix when passed to a View or Drawable, as it is implementation defined where in the hierarchy such canvases are created. It is recommended in such cases to either draw contents irrespective of the current matrix, or to track relevant transform state outside of the canvas.*

Return a new matrix with a copy of the canvas' current transformation matrix.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix) | This value cannot be`null`. |

### getMatrix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMatrix(ctm: Matrix): Unit
```

**Deprecated:** * [Hardware accelerated](https://developer.android.com/reference/kotlin/android/graphics/Canvas#isHardwareAccelerated())canvases may have any matrix when passed to a View or Drawable, as it is implementation defined where in the hierarchy such canvases are created. It is recommended in such cases to either draw contents irrespective of the current matrix, or to track relevant transform state outside of the canvas.*

Return, in ctm, the current transformation matrix. This does not alter the matrix in the canvas, but just returns a copy of it.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------|
| `ctm` | [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix):This value cannot be`null`. |

### getMaximumBitmapHeight

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMaximumBitmapHeight(): Int
```

Returns the maximum allowed height for bitmaps drawn with this canvas. Attempting to draw with a bitmap taller than this value will result in an error. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/Canvas#getMaximumBitmapWidth()> 

### getMaximumBitmapWidth

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMaximumBitmapWidth(): Int
```

Returns the maximum allowed width for bitmaps drawn with this canvas. Attempting to draw with a bitmap wider than this value will result in an error. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/Canvas#getMaximumBitmapHeight()> 

### getSaveCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSaveCount(): Int
```

Returns the number of matrix/clip states on the Canvas' private stack. This will equal # save() calls - # restore() calls. 

### getWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWidth(): Int
```

Returns the width of the current drawing layer

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the width of the current drawing layer |

### isHardwareAccelerated

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isHardwareAccelerated(): Boolean
```

Indicates whether this Canvas uses hardware acceleration. Note that this method does not define what type of hardware acceleration may or may not be used.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if drawing operations are hardware accelerated, false otherwise. |

### isOpaque

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isOpaque(): Boolean
```

Return true if the device that the current layer draws into is opaque (that is, it does not support per-pixel alpha).

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the device that the current layer draws into is opaque |

### quickReject

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun quickReject(path: Path): Boolean
```

Return true if the specified path, after being transformed by the current matrix, would lie completely outside of the current clip. Call this to check if an area you intend to draw into is clipped out (and therefore you can skip making the draw calls). Note: for speed it may return false even if the path itself might not intersect the clip (i.e. the bounds of the path intersects, but the path does not).

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path):The path to compare with the current clip This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the path (transformed by the canvas' matrix) does not intersect with the canvas' clip |

### quickReject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun quickReject(
    path: Path, 
    type: Canvas.EdgeType
): Boolean
```

**Deprecated:** *The EdgeType is ignored. Use [quickReject(android.graphics.Path)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#quickReject(android.graphics.Path))instead.*

Return true if the specified path, after being transformed by the current matrix, would lie completely outside of the current clip. Call this to check if an area you intend to draw into is clipped out (and therefore you can skip making the draw calls). Note: for speed it may return false even if the path itself might not intersect the clip (i.e. the bounds of the path intersects, but the path does not).

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path):The path to compare with the current clip This value cannot be`null`. |
| `type` | [Canvas.EdgeType](https://developer.android.com/reference/kotlin/android/graphics/Canvas.EdgeType): [Canvas.EdgeType.AA](https://developer.android.com/reference/kotlin/android/graphics/Canvas.EdgeType) if the path should be considered antialiased, since that means it may affect a larger area (more pixels) than non-antialiased ([Canvas.EdgeType.BW](https://developer.android.com/reference/kotlin/android/graphics/Canvas.EdgeType)). This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the path (transformed by the canvas' matrix) does not intersect with the canvas' clip |

### quickReject

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun quickReject(rect: RectF): Boolean
```

Return true if the specified rectangle, after being transformed by the current matrix, would lie completely outside of the current clip. Call this to check if an area you intend to draw into is clipped out (and therefore you can skip making the draw calls).

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rect` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF):the rect to compare with the current clip This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the rect (transformed by the canvas' matrix) does not intersect with the canvas' clip |

### quickReject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun quickReject(
    rect: RectF, 
    type: Canvas.EdgeType
): Boolean
```

**Deprecated:** *The EdgeType is ignored. Use [quickReject(android.graphics.RectF)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#quickReject(android.graphics.RectF))instead.*

Return true if the specified rectangle, after being transformed by the current matrix, would lie completely outside of the current clip. Call this to check if an area you intend to draw into is clipped out (and therefore you can skip making the draw calls).

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rect` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF):the rect to compare with the current clip This value cannot be`null`. |
| `type` | [Canvas.EdgeType](https://developer.android.com/reference/kotlin/android/graphics/Canvas.EdgeType): [Canvas.EdgeType.AA](https://developer.android.com/reference/kotlin/android/graphics/Canvas.EdgeType) if the path should be considered antialiased, since that means it may affect a larger area (more pixels) than non-antialiased ([Canvas.EdgeType.BW](https://developer.android.com/reference/kotlin/android/graphics/Canvas.EdgeType)). This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the rect (transformed by the canvas' matrix) does not intersect with the canvas' clip |

### quickReject

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun quickReject(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float
): Boolean
```

Return true if the specified rectangle, after being transformed by the current matrix, would lie completely outside of the current clip. Call this to check if an area you intend to draw into is clipped out (and therefore you can skip making the draw calls).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `left` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The left side of the rectangle to compare with the current clip |
| `top` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The top of the rectangle to compare with the current clip |
| `right` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The right side of the rectangle to compare with the current clip |
| `bottom` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The bottom of the rectangle to compare with the current clip |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the rect (transformed by the canvas' matrix) does not intersect with the canvas' clip |

### quickReject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun quickReject(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float, 
    type: Canvas.EdgeType
): Boolean
```

**Deprecated:** *The EdgeType is ignored. Use [quickReject(float,float,float,float)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#quickReject(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))instead.*

Return true if the specified rectangle, after being transformed by the current matrix, would lie completely outside of the current clip. Call this to check if an area you intend to draw into is clipped out (and therefore you can skip making the draw calls).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `left` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The left side of the rectangle to compare with the current clip |
| `top` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The top of the rectangle to compare with the current clip |
| `right` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The right side of the rectangle to compare with the current clip |
| `bottom` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The bottom of the rectangle to compare with the current clip |
| `type` | [Canvas.EdgeType](https://developer.android.com/reference/kotlin/android/graphics/Canvas.EdgeType): [Canvas.EdgeType.AA](https://developer.android.com/reference/kotlin/android/graphics/Canvas.EdgeType) if the path should be considered antialiased, since that means it may affect a larger area (more pixels) than non-antialiased ([Canvas.EdgeType.BW](https://developer.android.com/reference/kotlin/android/graphics/Canvas.EdgeType)). This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the rect (transformed by the canvas' matrix) does not intersect with the canvas' clip |

### restore

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun restore(): Unit
```

This call balances a previous call to save(), and is used to remove all modifications to the matrix/clip state since the last save call. It is an error to call restore() more times than save() was called. 

### restoreToCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun restoreToCount(saveCount: Int): Unit
```

Efficient way to pop any calls to save() that happened after the save count reached saveCount. It is an error for saveCount to be less than 1. Example: int count = canvas.save(); ... // more calls potentially to save() canvas.restoreToCount(count); // now the canvas is back in the same state it was before the initial // call to save().

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------|
| `saveCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The save level to restore to. |

### rotate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun rotate(degrees: Float): Unit
```

Preconcat the current matrix with the specified rotation.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------|
| `degrees` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The amount to rotate, in degrees |

### rotate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun rotate(
    degrees: Float, 
    px: Float, 
    py: Float
): Unit
```

Preconcat the current matrix with the specified rotation.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `degrees` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The amount to rotate, in degrees |
| `px` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-coord for the pivot point (unchanged by the rotation) |
| `py` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-coord for the pivot point (unchanged by the rotation) |

### save

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun save(): Int
```

Saves the current matrix and clip onto a private stack.

Subsequent calls to translate,scale,rotate,skew,concat or clipRect, clipPath will all operate as usual, but when the balancing call to restore() is made, those calls will be forgotten, and the settings that existed before the save() will be reinstated.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The value to pass to restoreToCount() to balance this save() |

### saveLayer

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun saveLayer(
    bounds: RectF?, 
    paint: Paint?
): Int
```

This behaves the same as save(), but in addition it allocates and redirects drawing to an offscreen rendering target.

**Note:** this method is very expensive, incurring more than double rendering cost for contained content. Avoid using this method when possible and instead use a [hardware layer](https://developer.android.com/reference/kotlin/android/view/View.html#LAYER_TYPE_HARDWARE:kotlin.Int) on a View to apply an xfermode, color filter, or alpha, as it will perform much better than this method.

All drawing calls are directed to a newly allocated offscreen rendering target. Only when the balancing call to restore() is made, is that offscreen buffer drawn back to the current target of the Canvas (which can potentially be a previous layer if these calls are nested).

Attributes of the Paint - [alpha](https://developer.android.com/reference/kotlin/android/graphics/Paint#getAlpha()), [Xfermode](https://developer.android.com/reference/kotlin/android/graphics/Paint#getXfermode()), and [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/Paint#getColorFilter())are applied when the offscreen rendering target is drawn back when restore() is called.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bounds` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)?:May be null. The maximum size the offscreen render target needs to be (in local coordinates) |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?:This is copied, and is applied to the offscreen when restore() is called. This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | value to pass to restoreToCount() to balance this save() |

### saveLayer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun saveLayer(
    bounds: RectF?, 
    paint: Paint?, 
    saveFlags: Int
): Int
```

**Deprecated:** *Use [saveLayer(android.graphics.RectF,android.graphics.Paint)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#saveLayer(android.graphics.RectF,%20android.graphics.Paint))instead.*

This behaves the same as save(), but in addition it allocates and redirects drawing to an offscreen bitmap.

**Note:** this method is very expensive, incurring more than double rendering cost for contained content. Avoid using this method, especially if the bounds provided are large. It is recommended to use a [hardware layer](https://developer.android.com/reference/kotlin/android/view/View.html#LAYER_TYPE_HARDWARE:kotlin.Int) on a View to apply an xfermode, color filter, or alpha, as it will perform much better than this method.

All drawing calls are directed to a newly allocated offscreen bitmap. Only when the balancing call to restore() is made, is that offscreen buffer drawn back to the current target of the Canvas (either the screen, it's target Bitmap, or the previous layer).

Attributes of the Paint - [alpha](https://developer.android.com/reference/kotlin/android/graphics/Paint#getAlpha()), [Xfermode](https://developer.android.com/reference/kotlin/android/graphics/Paint#getXfermode()), and [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/Paint#getColorFilter())are applied when the offscreen bitmap is drawn back when restore() is called. As of API Level API level {@value android.os.Build.VERSION_CODES#P Build.VERSION_CODES.P} the only valid`saveFlags`is [ALL_SAVE_FLAG](https://developer.android.com/reference/kotlin/android/graphics/Canvas#ALL_SAVE_FLAG:kotlin.Int). All other flags are ignored.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bounds` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)?:May be null. The maximum size the offscreen bitmap needs to be (in local coordinates) |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?:This is copied, and is applied to the offscreen when restore() is called. This value may be`null`. |
| `saveFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):see _SAVE_FLAG constants, generally [ALL_SAVE_FLAG](https://developer.android.com/reference/kotlin/android/graphics/Canvas#ALL_SAVE_FLAG:kotlin.Int) is recommended for performance reasons. Value is either`0`or [android.graphics.Canvas#ALL_SAVE_FLAG](https://developer.android.com/reference/kotlin/android/graphics/Canvas#ALL_SAVE_FLAG:kotlin.Int) |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | value to pass to restoreToCount() to balance this save() |

### saveLayer

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun saveLayer(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float, 
    paint: Paint?
): Int
```

Convenience for [saveLayer(android.graphics.RectF,android.graphics.Paint)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#saveLayer(android.graphics.RectF,%20android.graphics.Paint))that takes the four float coordinates of the bounds rectangle.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------|
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?:This value may be`null`. |

### saveLayer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun saveLayer(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float, 
    paint: Paint?, 
    saveFlags: Int
): Int
```

**Deprecated:** *Use [saveLayer(float,float,float,float,android.graphics.Paint)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#saveLayer(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Paint))instead.*

Helper version of saveLayer() that takes 4 values rather than a RectF. As of API Level API level {@value android.os.Build.VERSION_CODES#P Build.VERSION_CODES.P} the only valid`saveFlags`is [ALL_SAVE_FLAG](https://developer.android.com/reference/kotlin/android/graphics/Canvas#ALL_SAVE_FLAG:kotlin.Int). All other flags are ignored.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?:This value may be`null`. |
| `saveFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or [android.graphics.Canvas#ALL_SAVE_FLAG](https://developer.android.com/reference/kotlin/android/graphics/Canvas#ALL_SAVE_FLAG:kotlin.Int) |

### saveLayerAlpha

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun saveLayerAlpha(
    bounds: RectF?, 
    alpha: Int
): Int
```

Convenience for [saveLayer(android.graphics.RectF,android.graphics.Paint)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#saveLayer(android.graphics.RectF,%20android.graphics.Paint))but instead of taking a entire Paint object it takes only the`alpha`parameter.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bounds` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)?:The maximum size the offscreen bitmap needs to be (in local coordinates) This value may be`null`. |
| `alpha` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The alpha to apply to the offscreen when it is drawn during restore() |

### saveLayerAlpha

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun saveLayerAlpha(
    bounds: RectF?, 
    alpha: Int, 
    saveFlags: Int
): Int
```

**Deprecated:** *Use [saveLayerAlpha(android.graphics.RectF,int)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#saveLayerAlpha(android.graphics.RectF,%20kotlin.Int))instead.*

This behaves the same as save(), but in addition it allocates and redirects drawing to an offscreen bitmap.

**Note:** this method is very expensive, incurring more than double rendering cost for contained content. Avoid using this method, especially if the bounds provided are large. It is recommended to use a [hardware layer](https://developer.android.com/reference/kotlin/android/view/View.html#LAYER_TYPE_HARDWARE:kotlin.Int) on a View to apply an xfermode, color filter, or alpha, as it will perform much better than this method.

All drawing calls are directed to a newly allocated offscreen bitmap. Only when the balancing call to restore() is made, is that offscreen buffer drawn back to the current target of the Canvas (either the screen, it's target Bitmap, or the previous layer).

The`alpha`parameter is applied when the offscreen bitmap is drawn back when restore() is called. As of API Level API level {@value android.os.Build.VERSION_CODES#P Build.VERSION_CODES.P} the only valid`saveFlags`is [ALL_SAVE_FLAG](https://developer.android.com/reference/kotlin/android/graphics/Canvas#ALL_SAVE_FLAG:kotlin.Int). All other flags are ignored.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bounds` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)?:The maximum size the offscreen bitmap needs to be (in local coordinates) This value may be`null`. |
| `alpha` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The alpha to apply to the offscreen when it is drawn during restore() |
| `saveFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):see _SAVE_FLAG constants, generally [ALL_SAVE_FLAG](https://developer.android.com/reference/kotlin/android/graphics/Canvas#ALL_SAVE_FLAG:kotlin.Int) is recommended for performance reasons. Value is either`0`or [android.graphics.Canvas#ALL_SAVE_FLAG](https://developer.android.com/reference/kotlin/android/graphics/Canvas#ALL_SAVE_FLAG:kotlin.Int) |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | value to pass to restoreToCount() to balance this call |

### saveLayerAlpha

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun saveLayerAlpha(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float, 
    alpha: Int
): Int
```

Convenience for [saveLayerAlpha(android.graphics.RectF,int)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#saveLayerAlpha(android.graphics.RectF,%20kotlin.Int))that takes the four float coordinates of the bounds rectangle. 

### saveLayerAlpha

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun saveLayerAlpha(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float, 
    alpha: Int, 
    saveFlags: Int
): Int
```

**Deprecated:** *Use [saveLayerAlpha(float,float,float,float,int)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#saveLayerAlpha(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int))instead.*

Helper for saveLayerAlpha() that takes 4 values instead of a RectF. As of API Level API level {@value android.os.Build.VERSION_CODES#P Build.VERSION_CODES.P} the only valid`saveFlags`is [ALL_SAVE_FLAG](https://developer.android.com/reference/kotlin/android/graphics/Canvas#ALL_SAVE_FLAG:kotlin.Int). All other flags are ignored.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `saveFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or [android.graphics.Canvas#ALL_SAVE_FLAG](https://developer.android.com/reference/kotlin/android/graphics/Canvas#ALL_SAVE_FLAG:kotlin.Int) |

### scale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun scale(
    sx: Float, 
    sy: Float
): Unit
```

Preconcat the current matrix with the specified scale.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------|
| `sx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The amount to scale in X |
| `sy` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The amount to scale in Y |

### scale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun scale(
    sx: Float, 
    sy: Float, 
    px: Float, 
    py: Float
): Unit
```

Preconcat the current matrix with the specified scale.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `sx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The amount to scale in X |
| `sy` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The amount to scale in Y |
| `px` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-coord for the pivot point (unchanged by the scale) |
| `py` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-coord for the pivot point (unchanged by the scale) |

### setBitmap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setBitmap(bitmap: Bitmap?): Unit
```

Specify a bitmap for the canvas to draw into. All canvas state such as layers, filters, and the save/restore stack are reset. Additionally, the canvas' target density is updated to match that of the bitmap. Prior to API level {@value android.os.Build.VERSION_CODES#O Build.VERSION_CODES.O} the current matrix and clip stack were preserved.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bitmap` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap)?:Specifies a mutable bitmap for the canvas to draw into. This value may be`null`. |

**See Also**

- [#setDensity(int)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#setDensity(kotlin.Int))
- <https://developer.android.com/reference/kotlin/android/graphics/Canvas#getDensity()> 

### setDensity

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDensity(density: Int): Unit
```

Specifies the density for this Canvas' backing bitmap. This modifies the target density of the canvas itself, as well as the density of its backing bitmap via [Bitmap.setDensity(int)](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setDensity(kotlin.Int)).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `density` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new target density of the canvas, which is used to determine the scaling factor when drawing a bitmap into it. Use [Bitmap.DENSITY_NONE](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#DENSITY_NONE:kotlin.Int) to disable bitmap scaling. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/Canvas#getDensity()>
- [android.graphics.Bitmap#setDensity(int)](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setDensity(kotlin.Int)) 

### setDrawFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDrawFilter(filter: DrawFilter?): Unit
```

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------|
| `filter` | [DrawFilter](https://developer.android.com/reference/kotlin/android/graphics/DrawFilter)?:This value may be`null`. |

### setMatrix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMatrix(matrix: Matrix?): Unit
```

Completely replace the current matrix with the specified matrix. If the matrix parameter is null, then the current matrix is reset to identity.**Note:** it is recommended to use [concat(android.graphics.Matrix)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#concat(android.graphics.Matrix)), [scale(float,float)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#scale(kotlin.Float,%20kotlin.Float)), [translate(float,float)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#translate(kotlin.Float,%20kotlin.Float))and [rotate(float)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#rotate(kotlin.Float))instead of this method.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `matrix` | [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix)?:The matrix to replace the current matrix with. If it is null, set the current matrix to identity. |

**See Also**

- [#concat(Matrix)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#concat(android.graphics.Matrix)) 

### skew

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun skew(
    sx: Float, 
    sy: Float
): Unit
```

Preconcat the current matrix with the specified skew.

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------|
| `sx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The amount to skew in X |
| `sy` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The amount to skew in Y |

### translate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun translate(
    dx: Float, 
    dy: Float
): Unit
```

Preconcat the current matrix with the specified translation

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------|
| `dx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The distance to translate in X |
| `dy` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The distance to translate in Y |
