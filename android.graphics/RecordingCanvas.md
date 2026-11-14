Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RecordingCanvas

Kotlin | [Java](RecordingCanvas.md)
| --- | --- |

```
class RecordingCanvas : Canvas
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.Canvas](Canvas.md) ||
| | ↳ | [android.graphics.RecordingCanvas](RecordingCanvas.md) |

A Canvas implementation that records view system drawing operations for deferred rendering. This is used in combination with RenderNode. This class keeps a list of all the Paint and Bitmap objects that it draws, preventing the backing memory of Bitmaps from being released while the RecordingCanvas is still holding a native reference to the memory. This is obtained by calling beginRecording and is valid until the matching endRecording is called. It must not be retained beyond that as it is internally reused.

## Summary

| Inherited constants ||
|---|---|
| From class Canvas |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/Canvas#ALL_SAVE_FLAG:kotlin.Int` Restore everything when restore() is called (standard save flags). **Note:** for performance reasons, it is strongly recommended to pass this - the complete set of flags - to any call to `saveLayer()` and `saveLayerAlpha()` variants. **Note:** all methods that accept this flag have flagless versions that are equivalent to passing this flag. <br /> | ||

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | disableZ Disables Z support, preventing any RenderNodes drawn after this point from being visually reordered or having shadows rendered. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawARGB Fill the entire canvas' bitmap (restricted to the current clip) with the specified ARGB color, using srcover porterduff mode. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawArc Draw the specified arc, which will be scaled to fit inside the specified oval. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawArc Draw the specified arc, which will be scaled to fit inside the specified oval. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawBitmap Draw the bitmap using the specified matrix. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawBitmap Draw the specified bitmap, scaling/translating automatically to fill the destination rectangle. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawBitmap Draw the specified bitmap, scaling/translating automatically to fill the destination rectangle. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawBitmap Draw the specified bitmap, with its top/left corner at (x,y), using the specified paint, transformed by the current matrix. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawBitmap <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawBitmap <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawBitmapMesh Draw the bitmap through the mesh, where mesh vertices are evenly distributed across the bitmap. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawCircle Draw the specified circle using the specified paint. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawColor Fill the entire canvas' bitmap (restricted to the current clip) with the specified color, using srcover porterduff mode. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawColor Fill the entire canvas' bitmap (restricted to the current clip) with the specified color and blendmode. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawColor Fill the entire canvas' bitmap (restricted to the current clip) with the specified color and porter-duff xfermode. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawColor Fill the entire canvas' bitmap (restricted to the current clip) with the specified color and blendmode. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawDoubleRoundRect Draws a double rounded rectangle using the specified paint. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawDoubleRoundRect Draws a double rounded rectangle using the specified paint. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawGlyphs Draw array of glyphs with specified font. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawLine Draw a line segment with the specified start and stop x,y coordinates, using the specified paint. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawLines <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawLines Draw a series of lines. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawMesh Draws a mesh object to the screen. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawOval Draw the specified oval using the specified paint. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawOval Draw the specified oval using the specified paint. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawPaint Fill the entire canvas' bitmap (restricted to the current clip) with the specified paint. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawPatch Draws the specified bitmap as an N-patch (most often, a 9-patch.) |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawPatch Draws the specified bitmap as an N-patch (most often, a 9-patch.) |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawPath Draw the specified path using the specified paint. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawPicture Save the canvas state, draw the picture, and restore the canvas state. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawPicture Draw the picture, stretched to fit into the dst rectangle. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawPicture Draw the picture, stretched to fit into the dst rectangle. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawPoint Helper for drawPoints() for drawing a single point. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawPoints Helper for drawPoints() that assumes you want to draw the entire array |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawPoints Draw a series of points. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawPosText <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawPosText <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawRGB Fill the entire canvas' bitmap (restricted to the current clip) with the specified RGB color, using srcover porterduff mode. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawRect Draw the specified Rect using the specified Paint. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawRect Draw the specified Rect using the specified paint. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawRect Draw the specified Rect using the specified paint. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawRegion Draws the given region using the given paint. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawRenderNode Draws the specified display list onto this canvas. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawRoundRect Draw the specified round-rect using the specified paint. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawRoundRect Draw the specified round-rect using the specified paint. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawText Draw the text, with origin at (x,y), using the specified paint. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawText Draw the specified range of text, specified by start/end, with its origin at (x,y), in the specified Paint. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawText Draw the text, with origin at (x,y), using the specified paint. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawText Draw the text, with origin at (x,y), using the specified paint. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawTextOnPath Draw the text, with origin at (x,y), using the specified paint, along the specified path. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawTextOnPath Draw the text, with origin at (x,y), using the specified paint, along the specified path. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawTextRun Draw a run of text, all in a single direction, with optional context for complex text shaping. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawTextRun Draw a run of text, all in a single direction, with optional context for complex text shaping. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawTextRun Draw a run of text, all in a single direction, with optional context for complex text shaping. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | drawVertices Draw the array of vertices, interpreted as triangles (based on mode). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | enableZ Enables Z support which defaults to disabled. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getHeight Returns the height of the current drawing layer |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMaximumBitmapHeight Returns the maximum allowed height for bitmaps drawn with this canvas. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMaximumBitmapWidth Returns the maximum allowed width for bitmaps drawn with this canvas. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getWidth Returns the width of the current drawing layer |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isHardwareAccelerated Indicates whether this Canvas uses hardware acceleration. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isOpaque Return true if the device that the current layer draws into is opaque (that is, it does not support per-pixel alpha). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setBitmap Specify a bitmap for the canvas to draw into. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setDensity Specifies the density for this Canvas' backing bitmap. |

| Inherited functions ||
|---|---|
| From class Canvas |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | clipOutPath Set the clip to the difference of the current clip and the specified path. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | clipOutRect Set the clip to the difference of the current clip and the specified rectangle, which is expressed in local coordinates. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | clipOutRect Set the clip to the difference of the current clip and the specified rectangle, which is expressed in local coordinates. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | clipOutRect Set the clip to the difference of the current clip and the specified rectangle, which is expressed in local coordinates. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | clipOutRect Set the clip to the difference of the current clip and the specified rectangle, which is expressed in local coordinates. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | clipOutShader Set the clip to the difference of the current clip and the shader. The shader will be treated as an alpha mask, taking the difference of the two. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | clipPath Intersect the current clip with the specified path. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | clipPath Modify the current clip with the specified path. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | clipRect Intersect the current clip with the specified rectangle, which is expressed in local coordinates. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | clipRect Modify the current clip with the specified rectangle, which is expressed in local coordinates. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | clipRect Intersect the current clip with the specified rectangle, which is expressed in local coordinates. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | clipRect Modify the current clip with the specified rectangle. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | clipRect Intersect the current clip with the specified rectangle, which is expressed in local coordinates. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | clipRect Modify the current clip with the specified rectangle, which is expressed in local coordinates. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | clipRect Intersect the current clip with the specified rectangle, which is expressed in local coordinates. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | clipShader Intersect the current clip with the specified shader. The shader will be treated as an alpha mask, taking the intersection of the two. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | concat Preconcat the current matrix with the specified matrix. If the specified matrix is null, this method does nothing. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | concat Preconcat the current matrix with the specified matrix. If the specified matrix is null, this method does nothing. If the canvas's matrix is changed in the z-axis through this function, the deprecated getMatrix method will return a 3x3 with z-axis info stripped away. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | drawColor Fill the entire canvas' bitmap (restricted to the current clip) with the specified color, using srcover porterduff mode. <br /> | | Rect | getClipBounds Retrieve the bounds of the current clip (in local coordinates). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getClipBounds Return the bounds of the current clip (in local coordinates) in the bounds parameter, and return true if it is non-empty. This can be useful in a way similar to quickReject, in that it tells you that drawing outside of these bounds will be clipped out. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getDensity Returns the target density of the canvas. The default density is derived from the density of its backing bitmap, or `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#DENSITY_NONE:kotlin.Int` if there is not one. <br /> | | DrawFilter | getDrawFilter <br /> | | Matrix | getMatrix Return a new matrix with a copy of the canvas' current transformation matrix. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | getMatrix Return, in ctm, the current transformation matrix. This does not alter the matrix in the canvas, but just returns a copy of it. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getSaveCount Returns the number of matrix/clip states on the Canvas' private stack. This will equal # save() calls - # restore() calls. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | quickReject Return true if the specified path, after being transformed by the current matrix, would lie completely outside of the current clip. Call this to check if an area you intend to draw into is clipped out (and therefore you can skip making the draw calls). Note: for speed it may return false even if the path itself might not intersect the clip (i.e. the bounds of the path intersects, but the path does not). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | quickReject Return true if the specified path, after being transformed by the current matrix, would lie completely outside of the current clip. Call this to check if an area you intend to draw into is clipped out (and therefore you can skip making the draw calls). Note: for speed it may return false even if the path itself might not intersect the clip (i.e. the bounds of the path intersects, but the path does not). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | quickReject Return true if the specified rectangle, after being transformed by the current matrix, would lie completely outside of the current clip. Call this to check if an area you intend to draw into is clipped out (and therefore you can skip making the draw calls). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | quickReject Return true if the specified rectangle, after being transformed by the current matrix, would lie completely outside of the current clip. Call this to check if an area you intend to draw into is clipped out (and therefore you can skip making the draw calls). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | quickReject Return true if the specified rectangle, after being transformed by the current matrix, would lie completely outside of the current clip. Call this to check if an area you intend to draw into is clipped out (and therefore you can skip making the draw calls). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | quickReject Return true if the specified rectangle, after being transformed by the current matrix, would lie completely outside of the current clip. Call this to check if an area you intend to draw into is clipped out (and therefore you can skip making the draw calls). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | restore This call balances a previous call to save(), and is used to remove all modifications to the matrix/clip state since the last save call. It is an error to call restore() more times than save() was called. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | restoreToCount Efficient way to pop any calls to save() that happened after the save count reached saveCount. It is an error for saveCount to be less than 1. Example: int count = canvas.save(); ... // more calls potentially to save() canvas.restoreToCount(count); // now the canvas is back in the same state it was before the initial // call to save(). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | rotate Preconcat the current matrix with the specified rotation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | rotate Preconcat the current matrix with the specified rotation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | save Saves the current matrix and clip onto a private stack. Subsequent calls to translate,scale,rotate,skew,concat or clipRect, clipPath will all operate as usual, but when the balancing call to restore() is made, those calls will be forgotten, and the settings that existed before the save() will be reinstated. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | saveLayer This behaves the same as save(), but in addition it allocates and redirects drawing to an offscreen rendering target. **Note:** this method is very expensive, incurring more than double rendering cost for contained content. Avoid using this method when possible and instead use a `https://developer.android.com/reference/kotlin/android/view/View.html#LAYER_TYPE_HARDWARE:kotlin.Int` on a View to apply an xfermode, color filter, or alpha, as it will perform much better than this method. All drawing calls are directed to a newly allocated offscreen rendering target. Only when the balancing call to restore() is made, is that offscreen buffer drawn back to the current target of the Canvas (which can potentially be a previous layer if these calls are nested). Attributes of the Paint - getAlpha, getXfermode, and getColorFilter are applied when the offscreen rendering target is drawn back when restore() is called. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | saveLayer This behaves the same as save(), but in addition it allocates and redirects drawing to an offscreen bitmap. **Note:** this method is very expensive, incurring more than double rendering cost for contained content. Avoid using this method, especially if the bounds provided are large. It is recommended to use a `https://developer.android.com/reference/kotlin/android/view/View.html#LAYER_TYPE_HARDWARE:kotlin.Int` on a View to apply an xfermode, color filter, or alpha, as it will perform much better than this method. All drawing calls are directed to a newly allocated offscreen bitmap. Only when the balancing call to restore() is made, is that offscreen buffer drawn back to the current target of the Canvas (either the screen, it's target Bitmap, or the previous layer). Attributes of the Paint - getAlpha, getXfermode, and getColorFilter are applied when the offscreen bitmap is drawn back when restore() is called. As of API Level API level {@value Build.VERSION_CODES#P} the only valid `saveFlags` is `https://developer.android.com/reference/kotlin/android/graphics/Canvas#ALL_SAVE_FLAG:kotlin.Int`. All other flags are ignored. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | saveLayer Convenience for saveLayer that takes the four float coordinates of the bounds rectangle. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | saveLayer Helper version of saveLayer() that takes 4 values rather than a RectF. As of API Level API level {@value Build.VERSION_CODES#P} the only valid `saveFlags` is `https://developer.android.com/reference/kotlin/android/graphics/Canvas#ALL_SAVE_FLAG:kotlin.Int`. All other flags are ignored. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | saveLayerAlpha Convenience for saveLayer but instead of taking a entire Paint object it takes only the `alpha` parameter. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | saveLayerAlpha This behaves the same as save(), but in addition it allocates and redirects drawing to an offscreen bitmap. **Note:** this method is very expensive, incurring more than double rendering cost for contained content. Avoid using this method, especially if the bounds provided are large. It is recommended to use a `https://developer.android.com/reference/kotlin/android/view/View.html#LAYER_TYPE_HARDWARE:kotlin.Int` on a View to apply an xfermode, color filter, or alpha, as it will perform much better than this method. All drawing calls are directed to a newly allocated offscreen bitmap. Only when the balancing call to restore() is made, is that offscreen buffer drawn back to the current target of the Canvas (either the screen, it's target Bitmap, or the previous layer). The `alpha` parameter is applied when the offscreen bitmap is drawn back when restore() is called. As of API Level API level {@value Build.VERSION_CODES#P} the only valid `saveFlags` is `https://developer.android.com/reference/kotlin/android/graphics/Canvas#ALL_SAVE_FLAG:kotlin.Int`. All other flags are ignored. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | saveLayerAlpha Convenience for saveLayerAlpha that takes the four float coordinates of the bounds rectangle. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | saveLayerAlpha Helper for saveLayerAlpha() that takes 4 values instead of a RectF. As of API Level API level {@value Build.VERSION_CODES#P} the only valid `saveFlags` is `https://developer.android.com/reference/kotlin/android/graphics/Canvas#ALL_SAVE_FLAG:kotlin.Int`. All other flags are ignored. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | scale Preconcat the current matrix with the specified scale. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | scale Preconcat the current matrix with the specified scale. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setDrawFilter <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setMatrix Completely replace the current matrix with the specified matrix. If the matrix parameter is null, then the current matrix is reset to identity. **Note:** it is recommended to use concat, scale, translate and rotate instead of this method. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | skew Preconcat the current matrix with the specified skew. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | translate Preconcat the current matrix with the specified translation <br /> | ||

## Public methods

### disableZ

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun disableZ(): Unit
```

Disables Z support, preventing any RenderNodes drawn after this point from being visually reordered or having shadows rendered. Note: This is not impacted by any save or restore calls as it is not considered to be part of the current matrix or clip. See enableZ

### drawARGB

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawARGB(
    a: Int, 
    r: Int, 
    g: Int, 
    b: Int
): Unit
```

Fill the entire canvas' bitmap (restricted to the current clip) with the specified ARGB color, using srcover porterduff mode.

| Parameters ||
|---|---|
| `a` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): alpha component (0..255) of the color to draw onto the canvas |
| `r` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): red component (0..255) of the color to draw onto the canvas |
| `g` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): green component (0..255) of the color to draw onto the canvas |
| --- | --- |
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): blue component (0..255) of the color to draw onto the canvas |

### drawArc

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawArc(
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
|---|---|
| `oval` | [RectF](RectF.md): This value cannot be `null`. |
| `startAngle` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Starting angle (in degrees) where the arc begins |
| `sweepAngle` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Sweep angle (in degrees) measured clockwise |
| --- | --- |
| `useCenter` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, include the center of the oval in the arc, and close it if it is being stroked. This will draw a wedge |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |

### drawArc

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawArc(
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
|---|---|
| `startAngle` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Starting angle (in degrees) where the arc begins |
| `sweepAngle` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Sweep angle (in degrees) measured clockwise |
| `useCenter` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, include the center of the oval in the arc, and close it if it is being stroked. This will draw a wedge |
| --- | --- |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |

### drawBitmap

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawBitmap(
    bitmap: Bitmap, 
    matrix: Matrix, 
    paint: Paint?
): Unit
```

Draw the bitmap using the specified matrix.

| Parameters ||
|---|---|
| `bitmap` | [Bitmap](Bitmap.md): This value cannot be `null`. |
| `matrix` | [Matrix](Matrix.md): This value cannot be `null`. |
| `paint` | [Paint](Paint.md)?: This value may be `null`. |
| --- | --- |

### drawBitmap

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawBitmap(
    bitmap: Bitmap, 
    src: Rect?, 
    dst: Rect, 
    paint: Paint?
): Unit
```

Draw the specified bitmap, scaling/translating automatically to fill the destination rectangle. If the source rectangle is not null, it specifies the subset of the bitmap to draw.

Note: if the paint contains a maskfilter that generates a mask which extends beyond the bitmap's original width/height (e.g. BlurMaskFilter), then the bitmap will be drawn as if it were in a Shader with CLAMP mode. Thus the color outside of the original width/height will be the edge color replicated.

This function *ignores the density associated with the bitmap*. This is because the source and destination rectangle coordinate spaces are in their respective densities, so must already have the appropriate scaling factor applied.

| Parameters ||
|---|---|
| `bitmap` | [Bitmap](Bitmap.md): This value cannot be `null`. |
| `src` | [Rect](Rect.md)?: This value may be `null`. |
| `dst` | [Rect](Rect.md): This value cannot be `null`. |
| --- | --- |
| `paint` | [Paint](Paint.md)?: This value may be `null`. |

### drawBitmap

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawBitmap(
    bitmap: Bitmap, 
    src: Rect?, 
    dst: RectF, 
    paint: Paint?
): Unit
```

Draw the specified bitmap, scaling/translating automatically to fill the destination rectangle. If the source rectangle is not null, it specifies the subset of the bitmap to draw.

Note: if the paint contains a maskfilter that generates a mask which extends beyond the bitmap's original width/height (e.g. BlurMaskFilter), then the bitmap will be drawn as if it were in a Shader with CLAMP mode. Thus the color outside of the original width/height will be the edge color replicated.

This function *ignores the density associated with the bitmap*. This is because the source and destination rectangle coordinate spaces are in their respective densities, so must already have the appropriate scaling factor applied.

| Parameters ||
|---|---|
| `bitmap` | [Bitmap](Bitmap.md): This value cannot be `null`. |
| `src` | [Rect](Rect.md)?: This value may be `null`. |
| `dst` | [RectF](RectF.md): This value cannot be `null`. |
| --- | --- |
| `paint` | [Paint](Paint.md)?: This value may be `null`. |

### drawBitmap

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawBitmap(
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
|---|---|
| `bitmap` | [Bitmap](Bitmap.md): This value cannot be `null`. |
| `left` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The position of the left side of the bitmap being drawn |
| `top` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The position of the top side of the bitmap being drawn |
| --- | --- |
| `paint` | [Paint](Paint.md)?: This value may be `null`. |

### drawBitmap

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawBitmap(
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

**Deprecated:** *checkstyle*

| Parameters ||
|---|---|
| `colors` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): This value cannot be `null`. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Offset into the array of colors for the first pixel |
| `stride` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of colors in the array between rows (must be \>= width or \<= -width). |
| --- | --- |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The X coordinate for where to draw the bitmap |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The Y coordinate for where to draw the bitmap |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the bitmap |
| --- | --- |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the bitmap |
| `hasAlpha` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the alpha channel of the colors contains valid values. If false, the alpha byte is ignored (assumed to be 0xFF for every pixel). |
| `paint` | [Paint](Paint.md)?: This value may be `null`. |
| --- | --- |

### drawBitmap

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawBitmap(
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

**Deprecated:** *checkstyle*

| Parameters ||
|---|---|
| `colors` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): This value cannot be `null`. |
| `paint` | [Paint](Paint.md)?: This value may be `null`. |

### drawBitmapMesh

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawBitmapMesh(
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

Draw the bitmap through the mesh, where mesh vertices are evenly distributed across the bitmap. There are meshWidth+1 vertices across, and meshHeight+1 vertices down. The verts array is accessed in row-major order, so that the first meshWidth+1 vertices are distributed across the top of the bitmap from left to right. A more general version of this method is drawVertices(). Prior to API level {@value Build.VERSION_CODES#P} vertOffset and colorOffset were ignored, effectively treating them as zeros. In API level {@value Build.VERSION_CODES#P} and above these parameters will be respected.

Note: antialiasing is not supported, therefore `https://developer.android.com/reference/kotlin/android/graphics/Paint#ANTI_ALIAS_FLAG:kotlin.Int` is ignored.

| Parameters ||
|---|---|
| `bitmap` | [Bitmap](Bitmap.md): This value cannot be `null`. |
| `meshWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of columns in the mesh. Nothing is drawn if this is 0 |
| `meshHeight` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of rows in the mesh. Nothing is drawn if this is 0 |
| --- | --- |
| `verts` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): This value cannot be `null`. |
| `vertOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of verts elements to skip before drawing |
| `colors` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?: This value may be `null`. |
| --- | --- |
| `colorOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of color elements to skip before drawing |
| `paint` | [Paint](Paint.md)?: This value may be `null`. |

### drawCircle

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawCircle(
    cx: Float, 
    cy: Float, 
    radius: Float, 
    paint: Paint
): Unit
```

Draw the specified circle using the specified paint. If radius is \<= 0, then nothing will be drawn. The circle will be filled or framed based on the Style in the paint.

| Parameters ||
|---|---|
| `cx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The x-coordinate of the center of the circle to be drawn |
| `cy` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The y-coordinate of the center of the circle to be drawn |
| `radius` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The radius of the circle to be drawn |
| --- | --- |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |

### drawColor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawColor(color: Int): Unit
```

Fill the entire canvas' bitmap (restricted to the current clip) with the specified color, using srcover porterduff mode.

| Parameters ||
|---|---|
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the color to draw onto the canvas |

### drawColor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawColor(
    color: Int, 
    mode: BlendMode
): Unit
```

Fill the entire canvas' bitmap (restricted to the current clip) with the specified color and blendmode.

| Parameters ||
|---|---|
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the color to draw onto the canvas |
| `mode` | [BlendMode](BlendMode.md): This value cannot be `null`. |

### drawColor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawColor(
    color: Int, 
    mode: PorterDuff.Mode
): Unit
```

Fill the entire canvas' bitmap (restricted to the current clip) with the specified color and porter-duff xfermode.

| Parameters ||
|---|---|
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the color to draw onto the canvas |
| `mode` | [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md): This value cannot be `null`. |

### drawColor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawColor(
    color: Long, 
    mode: BlendMode
): Unit
```

Fill the entire canvas' bitmap (restricted to the current clip) with the specified color and blendmode.

| Parameters ||
|---|---|
| `color` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the `ColorLong` to draw onto the canvas. See the Color class for details about `ColorLong`s. |
| `mode` | [BlendMode](BlendMode.md): This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the color space encoded in the `ColorLong` is invalid or unknown. |

### drawDoubleRoundRect

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawDoubleRoundRect(
    outer: RectF, 
    outerRx: Float, 
    outerRy: Float, 
    inner: RectF, 
    innerRx: Float, 
    innerRy: Float, 
    paint: Paint
): Unit
```

Draws a double rounded rectangle using the specified paint. The resultant round rect will be filled in the area defined between the outer and inner rectangular bounds if the Paint configured with `https://developer.android.com/reference/kotlin/android/graphics/Paint.Style`. Otherwise if `https://developer.android.com/reference/kotlin/android/graphics/Paint.Style` is used, then 2 rounded rect strokes will be drawn at the outer and inner rounded rectangles

| Parameters ||
|---|---|
| `outer` | [RectF](RectF.md): This value cannot be `null`. |
| `outerRx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The x-radius of the oval used to round the corners on the outer rectangle |
| `outerRy` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The y-radius of the oval used to round the corners on the outer rectangle |
| --- | --- |
| `inner` | [RectF](RectF.md): This value cannot be `null`. |
| `innerRx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The x-radius of the oval used to round the corners on the inner rectangle |
| `innerRy` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The y-radius of the oval used to round the corners on the outer rectangle |
| --- | --- |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |

### drawDoubleRoundRect

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawDoubleRoundRect(
    outer: RectF, 
    outerRadii: FloatArray, 
    inner: RectF, 
    innerRadii: FloatArray, 
    paint: Paint
): Unit
```

Draws a double rounded rectangle using the specified paint. The resultant round rect will be filled in the area defined between the outer and inner rectangular bounds if the Paint configured with `https://developer.android.com/reference/kotlin/android/graphics/Paint.Style`. Otherwise if `https://developer.android.com/reference/kotlin/android/graphics/Paint.Style` is used, then 2 rounded rect strokes will be drawn at the outer and inner rounded rectangles

| Parameters ||
|---|---|
| `outer` | [RectF](RectF.md): This value cannot be `null`. |
| `outerRadii` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): This value cannot be `null`. |
| `inner` | [RectF](RectF.md): This value cannot be `null`. |
| --- | --- |
| `innerRadii` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): This value cannot be `null`. |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |

### drawGlyphs

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawGlyphs(
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
|---|---|
| `glyphIds` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): This value cannot be `null`. |
| `glyphIdOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is 0 or greater |
| `positions` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): This value cannot be `null`. |
| --- | --- |
| `positionOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is 0 or greater |
| `glyphCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is 0 or greater |
| `font` | [Font](../android.graphics.fonts/Font.md): This value cannot be `null`. |
| --- | --- |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |

### drawLine

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawLine(
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
|---|---|
| `startX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The x-coordinate of the start point of the line |
| `startY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The y-coordinate of the start point of the line |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |
| --- | --- |

### drawLines

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawLines(
    pts: FloatArray, 
    paint: Paint
): Unit
```

| Parameters ||
|---|---|
| `pts` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): This value cannot be `null`. |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |

### drawLines

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawLines(
    pts: FloatArray, 
    offset: Int, 
    count: Int, 
    paint: Paint
): Unit
```

Draw a series of lines. Each line is taken from 4 consecutive values in the pts array. Thus to draw 1 line, the array must contain at least 4 values. This is logically the same as drawing the array as follows: drawLine(pts\[0\], pts\[1\], pts\[2\], pts\[3\]) followed by drawLine(pts\[4\], pts\[5\], pts\[6\], pts\[7\]) and so on.

| Parameters ||
|---|---|
| `pts` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): This value cannot be `null`. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of values in the array to skip before drawing. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of values in the array to process, after skipping "offset" of them. Since each line uses 4 values, the number of "lines" that are drawn is really (count \>\> 2). |
| --- | --- |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |

### drawMesh

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawMesh(
    mesh: Mesh, 
    blendMode: BlendMode?, 
    paint: Paint
): Unit
```

Draws a mesh object to the screen.

Note: antialiasing is not supported, therefore `https://developer.android.com/reference/kotlin/android/graphics/Paint#ANTI_ALIAS_FLAG:kotlin.Int` is ignored.

| Parameters ||
|---|---|
| `mesh` | [Mesh](Mesh.md): This value cannot be `null`. |
| `blendMode` | [BlendMode](BlendMode.md)?: This value may be `null`. |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |
| --- | --- |

### drawOval

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawOval(
    oval: RectF, 
    paint: Paint
): Unit
```

Draw the specified oval using the specified paint. The oval will be filled or framed based on the Style in the paint.

| Parameters ||
|---|---|
| `oval` | [RectF](RectF.md): This value cannot be `null`. |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |

### drawOval

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawOval(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float, 
    paint: Paint
): Unit
```

Draw the specified oval using the specified paint. The oval will be filled or framed based on the Style in the paint.

| Parameters ||
|---|---|
| `paint` | [Paint](Paint.md): This value cannot be `null`. |

### drawPaint

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawPaint(paint: Paint): Unit
```

Fill the entire canvas' bitmap (restricted to the current clip) with the specified paint. This is equivalent (but faster) to drawing an infinitely large rectangle with the specified paint.

| Parameters ||
|---|---|
| `paint` | [Paint](Paint.md): This value cannot be `null`. |

### drawPatch

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawPatch(
    patch: NinePatch, 
    dst: Rect, 
    paint: Paint?
): Unit
```

Draws the specified bitmap as an N-patch (most often, a 9-patch.)

Note: antialiasing is not supported, therefore `https://developer.android.com/reference/kotlin/android/graphics/Paint#ANTI_ALIAS_FLAG:kotlin.Int` is ignored.

| Parameters ||
|---|---|
| `patch` | [NinePatch](NinePatch.md): This value cannot be `null`. |
| `dst` | [Rect](Rect.md): This value cannot be `null`. |
| `paint` | [Paint](Paint.md)?: This value may be `null`. |
| --- | --- |

### drawPatch

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawPatch(
    patch: NinePatch, 
    dst: RectF, 
    paint: Paint?
): Unit
```

Draws the specified bitmap as an N-patch (most often, a 9-patch.)

Note: antialiasing is not supported, therefore `https://developer.android.com/reference/kotlin/android/graphics/Paint#ANTI_ALIAS_FLAG:kotlin.Int` is ignored.

| Parameters ||
|---|---|
| `patch` | [NinePatch](NinePatch.md): This value cannot be `null`. |
| `dst` | [RectF](RectF.md): This value cannot be `null`. |
| `paint` | [Paint](Paint.md)?: This value may be `null`. |
| --- | --- |

### drawPath

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawPath(
    path: Path, 
    paint: Paint
): Unit
```

Draw the specified path using the specified paint. The path will be filled or framed based on the Style in the paint.

| Parameters ||
|---|---|
| `path` | [Path](Path.md): This value cannot be `null`. |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |

### drawPicture

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawPicture(picture: Picture): Unit
```

Save the canvas state, draw the picture, and restore the canvas state. This differs from picture.draw(canvas), which does not perform any save/restore.

**Note:** This forces the picture to internally call endRecording in order to prepare for playback.

| Parameters ||
|---|---|
| `picture` | [Picture](Picture.md): This value cannot be `null`. |

### drawPicture

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawPicture(
    picture: Picture, 
    dst: Rect
): Unit
```

Draw the picture, stretched to fit into the dst rectangle.

| Parameters ||
|---|---|
| `picture` | [Picture](Picture.md): This value cannot be `null`. |
| `dst` | [Rect](Rect.md): This value cannot be `null`. |

### drawPicture

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawPicture(
    picture: Picture, 
    dst: RectF
): Unit
```

Draw the picture, stretched to fit into the dst rectangle.

| Parameters ||
|---|---|
| `picture` | [Picture](Picture.md): This value cannot be `null`. |
| `dst` | [RectF](RectF.md): This value cannot be `null`. |

### drawPoint

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawPoint(
    x: Float, 
    y: Float, 
    paint: Paint
): Unit
```

Helper for drawPoints() for drawing a single point.

| Parameters ||
|---|---|
| `paint` | [Paint](Paint.md): This value cannot be `null`. |

### drawPoints

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawPoints(
    pts: FloatArray, 
    paint: Paint
): Unit
```

Helper for drawPoints() that assumes you want to draw the entire array

| Parameters ||
|---|---|
| `pts` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): This value cannot be `null`. |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |

### drawPoints

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawPoints(
    pts: FloatArray!, 
    offset: Int, 
    count: Int, 
    paint: Paint
): Unit
```

Draw a series of points. Each point is centered at the coordinate specified by pts\[\], and its diameter is specified by the paint's stroke width (as transformed by the canvas' CTM), with special treatment for a stroke width of 0, which always draws exactly 1 pixel (or at most 4 if antialiasing is enabled). The shape of the point is controlled by the paint's Cap type. The shape is a square, unless the cap type is Round, in which case the shape is a circle.

| Parameters ||
|---|---|
| `pts` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!: Array of points to draw \[x0 y0 x1 y1 x2 y2 ...\] |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of values to skip before starting to draw. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of values to process, after skipping offset of them. Since one point uses two values, the number of "points" that are drawn is really (count \>\> 1). |
| --- | --- |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |

### drawPosText

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawPosText(
    text: CharArray, 
    index: Int, 
    count: Int, 
    pos: FloatArray, 
    paint: Paint
): Unit
```

**Deprecated:** *checkstyle*

| Parameters ||
|---|---|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): This value cannot be `null`. |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the first character to draw |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of characters to draw, starting from index. |
| --- | --- |
| `pos` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): This value cannot be `null`. |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |

### drawPosText

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawPosText(
    text: String, 
    pos: FloatArray, 
    paint: Paint
): Unit
```

**Deprecated:** *checkstyle*

| Parameters ||
|---|---|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `pos` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): This value cannot be `null`. |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |
| --- | --- |

### drawRGB

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawRGB(
    r: Int, 
    g: Int, 
    b: Int
): Unit
```

Fill the entire canvas' bitmap (restricted to the current clip) with the specified RGB color, using srcover porterduff mode.

| Parameters ||
|---|---|
| `r` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): red component (0..255) of the color to draw onto the canvas |
| `g` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): green component (0..255) of the color to draw onto the canvas |
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): blue component (0..255) of the color to draw onto the canvas |
| --- | --- |

### drawRect

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawRect(
    r: Rect, 
    paint: Paint
): Unit
```

Draw the specified Rect using the specified Paint. The rectangle will be filled or framed based on the Style in the paint.

| Parameters ||
|---|---|
| `r` | [Rect](Rect.md): This value cannot be `null`. |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |

### drawRect

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawRect(
    rect: RectF, 
    paint: Paint
): Unit
```

Draw the specified Rect using the specified paint. The rectangle will be filled or framed based on the Style in the paint.

| Parameters ||
|---|---|
| `rect` | [RectF](RectF.md): This value cannot be `null`. |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |

### drawRect

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawRect(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float, 
    paint: Paint
): Unit
```

Draw the specified Rect using the specified paint. The rectangle will be filled or framed based on the Style in the paint.

| Parameters ||
|---|---|
| `left` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The left side of the rectangle to be drawn |
| `top` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The top side of the rectangle to be drawn |
| `right` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The right side of the rectangle to be drawn |
| --- | --- |
| `bottom` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The bottom side of the rectangle to be drawn |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |

### drawRegion

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawRegion(
    region: Region, 
    paint: Paint
): Unit
```

Draws the given region using the given paint.

| Parameters ||
|---|---|
| `region` | [Region](Region.md): This value cannot be `null`. |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |

### drawRenderNode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawRenderNode(renderNode: RenderNode): Unit
```

Draws the specified display list onto this canvas.

| Parameters ||
|---|---|
| `renderNode` | [RenderNode](RenderNode.md): The RenderNode to draw. This value cannot be `null`. |

### drawRoundRect

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawRoundRect(
    rect: RectF, 
    rx: Float, 
    ry: Float, 
    paint: Paint
): Unit
```

Draw the specified round-rect using the specified paint. The roundrect will be filled or framed based on the Style in the paint.

| Parameters ||
|---|---|
| `rect` | [RectF](RectF.md): This value cannot be `null`. |
| `rx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The x-radius of the oval used to round the corners |
| `ry` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The y-radius of the oval used to round the corners |
| --- | --- |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |

### drawRoundRect

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawRoundRect(
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
|---|---|
| `rx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The x-radius of the oval used to round the corners |
| `ry` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The y-radius of the oval used to round the corners |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |
| --- | --- |

### drawText

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawText(
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
|---|---|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): This value cannot be `null`. |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The x-coordinate of the origin of the text being drawn |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The y-coordinate of the baseline of the text being drawn |
| --- | --- |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |

### drawText

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawText(
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
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): This value cannot be `null`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the first character in text to draw |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): (end - 1) is the index of the last character in text to draw |
| --- | --- |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The x-coordinate of origin for where to draw the text |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The y-coordinate of origin for where to draw the text |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |
| --- | --- |

### drawText

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawText(
    text: String, 
    x: Float, 
    y: Float, 
    paint: Paint
): Unit
```

Draw the text, with origin at (x,y), using the specified paint. The origin is interpreted based on the Align setting in the paint.

| Parameters ||
|---|---|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The x-coordinate of the origin of the text being drawn |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The y-coordinate of the baseline of the text being drawn |
| --- | --- |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |

### drawText

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawText(
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
|---|---|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the first character in text to draw |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): (end - 1) is the index of the last character in text to draw |
| --- | --- |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The x-coordinate of the origin of the text being drawn |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The y-coordinate of the baseline of the text being drawn |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |
| --- | --- |

### drawTextOnPath

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawTextOnPath(
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
|---|---|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): This value cannot be `null`. |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The starting index within the text to be drawn |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Starting from index, the number of characters to draw |
| --- | --- |
| `path` | [Path](Path.md): This value cannot be `null`. |
| `hOffset` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The distance along the path to add to the text's starting position |
| `vOffset` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The distance above(-) or below(+) the path to position the text |
| --- | --- |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |

### drawTextOnPath

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawTextOnPath(
    text: String, 
    path: Path, 
    hOffset: Float, 
    vOffset: Float, 
    paint: Paint
): Unit
```

Draw the text, with origin at (x,y), using the specified paint, along the specified path. The paint's Align setting determines where along the path to start the text.

| Parameters ||
|---|---|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `path` | [Path](Path.md): This value cannot be `null`. |
| `hOffset` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The distance along the path to add to the text's starting position |
| --- | --- |
| `vOffset` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The distance above(-) or below(+) the path to position the text |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |

### drawTextRun

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawTextRun(
    measuredText: MeasuredText, 
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

See drawTextRun for more details. This method uses a MeasuredText rather than CharSequence to represent the string.

| Parameters ||
|---|---|
| `text` | the text to render. This value cannot be `null`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start of the text to render. Data before this position can be used for shaping context. |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the end of the text to render. Data at or after this position can be used for shaping context. |
| --- | --- |
| `contextStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the start of the shaping context |
| `contextEnd` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the end of the shaping context |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the x position at which to draw the text |
| --- | --- |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the y position at which to draw the text |
| `isRtl` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether the run is in RTL direction |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |
| --- | --- |
| `measuredText` | [MeasuredText](../android.graphics.text/MeasuredText.md): This value cannot be `null`. |

### drawTextRun

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawTextRun(
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

See drawTextRun for more details. This method uses a character array rather than CharSequence to represent the string. Also, to be consistent with the pattern established in #drawText, in this method `count` and `contextCount` are used rather than offsets of the end position; `count = end - start, contextCount = contextEnd - contextStart`.

| Parameters ||
|---|---|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): This value cannot be `null`. |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start of the text to render |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the count of chars to render |
| --- | --- |
| `contextIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start of the context for shaping. Must be no greater than index. |
| `contextCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of characters in the context for shaping. contexIndex + contextCount must be no less than index + count. |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the x position at which to draw the text |
| --- | --- |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the y position at which to draw the text |
| `isRtl` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether the run is in RTL direction |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |
| --- | --- |

### drawTextRun

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawTextRun(
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

The run of text includes the characters from `start` to `end` in the text. In addition, the range `contextStart` to `contextEnd` is used as context for the purpose of complex text shaping, such as Arabic text potentially shaped differently based on the text next to it.

All text outside the range `contextStart..contextEnd` is ignored. The text between `start` and `end` will be laid out and drawn. The context range is useful for contextual shaping, e.g. Kerning, Arabic contextural form.

The direction of the run is explicitly specified by `isRtl`. Thus, this method is suitable only for runs of a single direction. Alignment of the text is as determined by the Paint's TextAlign value. Further, `0 <= contextStart <= start <= end <= contextEnd <= text.length` must hold on entry.

Also see android.graphics.Paint#getRunAdvance for a corresponding method to measure the text; the advance width of the text drawn matches the value obtained from that method.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): This value cannot be `null`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start of the text to render. Data before this position can be used for shaping context. |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the end of the text to render. Data at or after this position can be used for shaping context. |
| --- | --- |
| `contextStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the start of the shaping context |
| `contextEnd` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the end of the shaping context |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the x position at which to draw the text |
| --- | --- |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the y position at which to draw the text |
| `isRtl` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether the run is in RTL direction |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |
| --- | --- |

### drawVertices

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun drawVertices(
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

Note: antialiasing is not supported, therefore `https://developer.android.com/reference/kotlin/android/graphics/Paint#ANTI_ALIAS_FLAG:kotlin.Int` is ignored.

| Parameters ||
|---|---|
| `mode` | [Canvas.VertexMode](../android/graphics/Canvas.VertexMode.md): This value cannot be `null`. |
| `vertexCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of values in the vertices array (and corresponding texs and colors arrays if non-null). Each logical vertex is two values (x, y), vertexCount must be a multiple of 2. |
| `verts` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): This value cannot be `null`. |
| --- | --- |
| `vertOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of values in the verts to skip before drawing. |
| `texs` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?: This value may be `null`. |
| `texOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of values in texs to skip before drawing. |
| --- | --- |
| `colors` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?: This value may be `null`. |
| `colorOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of values in colors to skip before drawing. |
| `indices` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)?: This value may be `null`. |
| --- | --- |
| `indexCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of entries in the indices array (if not null). |
| `paint` | [Paint](Paint.md): This value cannot be `null`. |

### enableZ

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun enableZ(): Unit
```

Enables Z support which defaults to disabled. This allows for RenderNodes drawn with drawRenderNode to be re-arranged based off of their getElevation and getTranslationZ values. It also enables rendering of shadows for RenderNodes with an elevation or translationZ.

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

Note: This is not impacted by any save or restore calls as it is not considered to be part of the current matrix or clip. See disableZ

### getHeight

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHeight(): Int
```

Returns the height of the current drawing layer

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the height of the current drawing layer |

### getMaximumBitmapHeight

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMaximumBitmapHeight(): Int
```

Returns the maximum allowed height for bitmaps drawn with this canvas. Attempting to draw with a bitmap taller than this value will result in an error.

### getMaximumBitmapWidth

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMaximumBitmapWidth(): Int
```

Returns the maximum allowed width for bitmaps drawn with this canvas. Attempting to draw with a bitmap wider than this value will result in an error.

### getWidth

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getWidth(): Int
```

Returns the width of the current drawing layer

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the width of the current drawing layer |

### isHardwareAccelerated

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isHardwareAccelerated(): Boolean
```

Indicates whether this Canvas uses hardware acceleration. Note that this method does not define what type of hardware acceleration may or may not be used.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if drawing operations are hardware accelerated, false otherwise. |

### isOpaque

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isOpaque(): Boolean
```

Return true if the device that the current layer draws into is opaque (that is, it does not support per-pixel alpha).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the device that the current layer draws into is opaque |

### setBitmap

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setBitmap(bitmap: Bitmap?): Unit
```

Specify a bitmap for the canvas to draw into. All canvas state such as layers, filters, and the save/restore stack are reset. Additionally, the canvas' target density is updated to match that of the bitmap. Prior to API level {@value Build.VERSION_CODES#O} the current matrix and clip stack were preserved.

| Parameters ||
|---|---|
| `bitmap` | [Bitmap](Bitmap.md)?: Specifies a mutable bitmap for the canvas to draw into. This value may be `null`. |

### setDensity

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setDensity(density: Int): Unit
```

Specifies the density for this Canvas' backing bitmap. This modifies the target density of the canvas itself, as well as the density of its backing bitmap via setDensity.

| Parameters ||
|---|---|
| `density` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new target density of the canvas, which is used to determine the scaling factor when drawing a bitmap into it. Use `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#DENSITY_NONE:kotlin.Int` to disable bitmap scaling. |
