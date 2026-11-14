Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Path

Kotlin | [Java](https://developer.android.com/reference/android/graphics/Path "View this page in Java")
| --- | --- |

```
open class Path
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.Path](https://developer.android.com/reference/kotlin/android/graphics/Path#) |

The Path class encapsulates compound (multiple contour) geometric paths consisting of straight line segments, quadratic curves, and cubic curves. It can be drawn with canvas.drawPath(path, paint), either filled or stroked (based on the paint's Style), or it can be used for clipping or to draw text on a path.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/graphics/Path.Direction` Specifies how closed shapes (e.g. rects, ovals) are oriented when they are added to a path. |
| | `https://developer.android.com/reference/kotlin/android/graphics/Path.FillType` Enum for the ways a path may be filled. |
| | `https://developer.android.com/reference/kotlin/android/graphics/Path.Op` The logical operations that can be performed when combining two paths. |
| --- | --- |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Path#Path()()` Create an empty path |
| `https://developer.android.com/reference/kotlin/android/graphics/Path#Path(android.graphics.Path)(src: https://developer.android.com/reference/kotlin/android/graphics/Path#?)` Create a new path, copying the contents from the src path. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#addArc(android.graphics.RectF,%20kotlin.Float,%20kotlin.Float)(oval: https://developer.android.com/reference/kotlin/android/graphics/RectF, startAngle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, sweepAngle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Add the specified arc to the path as a new contour. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#addArc(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float)(left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, startAngle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, sweepAngle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Add the specified arc to the path as a new contour. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#addCircle(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Path.Direction)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, radius: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dir: https://developer.android.com/reference/kotlin/android/graphics/Path.Direction)` Add a closed circle contour to the path |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#addOval(android.graphics.RectF,%20android.graphics.Path.Direction)(oval: https://developer.android.com/reference/kotlin/android/graphics/RectF, dir: https://developer.android.com/reference/kotlin/android/graphics/Path.Direction)` Add a closed oval contour to the path |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#addOval(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Path.Direction)(left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dir: https://developer.android.com/reference/kotlin/android/graphics/Path.Direction)` Add a closed oval contour to the path |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#addPath(android.graphics.Path)(src: https://developer.android.com/reference/kotlin/android/graphics/Path#)` Add a copy of src to the path |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#addPath(android.graphics.Path,%20android.graphics.Matrix)(src: https://developer.android.com/reference/kotlin/android/graphics/Path#, matrix: https://developer.android.com/reference/kotlin/android/graphics/Matrix)` Add a copy of src to the path, transformed by matrix |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#addPath(android.graphics.Path,%20kotlin.Float,%20kotlin.Float)(src: https://developer.android.com/reference/kotlin/android/graphics/Path#, dx: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Add a copy of src to the path, offset by (dx,dy) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#addRect(android.graphics.RectF,%20android.graphics.Path.Direction)(rect: https://developer.android.com/reference/kotlin/android/graphics/RectF, dir: https://developer.android.com/reference/kotlin/android/graphics/Path.Direction)` Add a closed rectangle contour to the path |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#addRect(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Path.Direction)(left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dir: https://developer.android.com/reference/kotlin/android/graphics/Path.Direction)` Add a closed rectangle contour to the path |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#addRoundRect(android.graphics.RectF,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Path.Direction)(rect: https://developer.android.com/reference/kotlin/android/graphics/RectF, rx: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, ry: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dir: https://developer.android.com/reference/kotlin/android/graphics/Path.Direction)` Add a closed round-rectangle contour to the path |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#addRoundRect(android.graphics.RectF,%20kotlin.FloatArray,%20android.graphics.Path.Direction)(rect: https://developer.android.com/reference/kotlin/android/graphics/RectF, radii: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html, dir: https://developer.android.com/reference/kotlin/android/graphics/Path.Direction)` Add a closed round-rectangle contour to the path. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#addRoundRect(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Path.Direction)(left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, rx: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, ry: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dir: https://developer.android.com/reference/kotlin/android/graphics/Path.Direction)` Add a closed round-rectangle contour to the path |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#addRoundRect(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.FloatArray,%20android.graphics.Path.Direction)(left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, radii: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html, dir: https://developer.android.com/reference/kotlin/android/graphics/Path.Direction)` Add a closed round-rectangle contour to the path. |
| open [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#approximate(kotlin.Float)(acceptableError: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Approximate the `Path` with a series of line segments. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#arcTo(android.graphics.RectF,%20kotlin.Float,%20kotlin.Float)(oval: https://developer.android.com/reference/kotlin/android/graphics/RectF, startAngle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, sweepAngle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Append the specified arc to the path as a new contour. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#arcTo(android.graphics.RectF,%20kotlin.Float,%20kotlin.Float,%20kotlin.Boolean)(oval: https://developer.android.com/reference/kotlin/android/graphics/RectF, startAngle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, sweepAngle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, forceMoveTo: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Append the specified arc to the path as a new contour. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#arcTo(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Boolean)(left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, startAngle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, sweepAngle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, forceMoveTo: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Append the specified arc to the path as a new contour. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#close()()` Close the current contour. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#computeBounds(android.graphics.RectF)(bounds: https://developer.android.com/reference/kotlin/android/graphics/RectF)` Compute the bounds of the control points of the path, and write the answer into bounds. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#computeBounds(android.graphics.RectF,%20kotlin.Boolean)(bounds: https://developer.android.com/reference/kotlin/android/graphics/RectF, exact: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Compute the bounds of the control points of the path, and write the answer into bounds. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#conicTo(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float)(x1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, x2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, weight: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Add a quadratic bezier from the last point, approaching control point (x1,y1), and ending at (x2,y2), weighted by `weight`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#cubicTo(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float)(x1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, x2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, x3: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y3: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Add a cubic bezier from the last point, approaching control points (x1,y1) and (x2,y2), and ending at (x3,y3). |
| open [Path.FillType](https://developer.android.com/reference/kotlin/android/graphics/Path.FillType) | `https://developer.android.com/reference/kotlin/android/graphics/Path#getFillType()()` Return the path's fill type. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#getGenerationId()()` Returns the generation ID of this path. |
| open [PathIterator](https://developer.android.com/reference/kotlin/android/graphics/PathIterator) | `https://developer.android.com/reference/kotlin/android/graphics/Path#getPathIterator()()` Returns an iterator over the segments of this path. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#incReserve(kotlin.Int)(extraPtCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Hint to the path to prepare for adding more points. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#interpolate(android.graphics.Path,%20kotlin.Float,%20android.graphics.Path)(otherPath: https://developer.android.com/reference/kotlin/android/graphics/Path#, t: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, interpolatedPath: https://developer.android.com/reference/kotlin/android/graphics/Path#)` This method will linearly interpolate from this path to `otherPath` given the interpolation parameter `t`, returning the result in `interpolatedPath`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#isConvex()()` Returns the path's convexity, as defined by the content of the path. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#isEmpty()()` Returns true if the path is empty (contains no lines or curves) |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#isInterpolatable(android.graphics.Path)(otherPath: https://developer.android.com/reference/kotlin/android/graphics/Path#)` Two paths can be interpolated, by calling `https://developer.android.com/reference/kotlin/android/graphics/Path#interpolate(android.graphics.Path,%20kotlin.Float,%20android.graphics.Path)`, if they have exactly the same structure. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#isInverseFillType()()` Returns true if the filltype is one of the INVERSE variants |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#isRect(android.graphics.RectF)(rect: https://developer.android.com/reference/kotlin/android/graphics/RectF?)` Returns true if the path specifies a rectangle. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#lineTo(kotlin.Float,%20kotlin.Float)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Add a line from the last point to the specified point (x,y). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#moveTo(kotlin.Float,%20kotlin.Float)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Set the beginning of the next contour to the point (x,y). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#offset(kotlin.Float,%20kotlin.Float)(dx: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Offset the path by (dx,dy) |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#offset(kotlin.Float,%20kotlin.Float,%20android.graphics.Path)(dx: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dst: https://developer.android.com/reference/kotlin/android/graphics/Path#?)` Offset the path by (dx,dy) |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#op(android.graphics.Path,%20android.graphics.Path,%20android.graphics.Path.Op)(path1: https://developer.android.com/reference/kotlin/android/graphics/Path#, path2: https://developer.android.com/reference/kotlin/android/graphics/Path#, op: https://developer.android.com/reference/kotlin/android/graphics/Path.Op)` Set this path to the result of applying the Op to the two specified paths. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#op(android.graphics.Path,%20android.graphics.Path.Op)(path: https://developer.android.com/reference/kotlin/android/graphics/Path#, op: https://developer.android.com/reference/kotlin/android/graphics/Path.Op)` Set this path to the result of applying the Op to this path and the specified path. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#quadTo(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float)(x1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, x2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Add a quadratic bezier from the last point, approaching control point (x1,y1), and ending at (x2,y2). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#rConicTo(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float)(dx1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dy1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dx2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dy2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, weight: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Same as conicTo, but the coordinates are considered relative to the last point on this contour. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#rCubicTo(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float)(x1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, x2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, x3: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y3: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Same as cubicTo, but the coordinates are considered relative to the current point on this contour. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#rLineTo(kotlin.Float,%20kotlin.Float)(dx: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Same as lineTo, but the coordinates are considered relative to the last point on this contour. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#rMoveTo(kotlin.Float,%20kotlin.Float)(dx: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Set the beginning of the next contour relative to the last point on the previous contour. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#rQuadTo(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float)(dx1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dy1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dx2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dy2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Same as quadTo, but the coordinates are considered relative to the last point on this contour. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#reset()()` Clear any lines and curves from the path, making it empty. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#rewind()()` Rewinds the path: clears any lines and curves from the path but keeps the internal data structure for faster reuse. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#set(android.graphics.Path)(src: https://developer.android.com/reference/kotlin/android/graphics/Path#)` Replace the contents of this with the contents of src. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#setFillType(android.graphics.Path.FillType)(ft: https://developer.android.com/reference/kotlin/android/graphics/Path.FillType)` Set the path's fill type. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#setLastPoint(kotlin.Float,%20kotlin.Float)(dx: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the last point of the path. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#toggleInverseFillType()()` Toggles the INVERSE state of the filltype |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#transform(android.graphics.Matrix)(matrix: https://developer.android.com/reference/kotlin/android/graphics/Matrix)` Transform the points in this path by matrix. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Path#transform(android.graphics.Matrix,%20android.graphics.Path)(matrix: https://developer.android.com/reference/kotlin/android/graphics/Matrix, dst: https://developer.android.com/reference/kotlin/android/graphics/Path#?)` Transform the points in this path by matrix, and write the answer into dst. |

## Public constructors

### Path

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Path()
```

Create an empty path

### Path

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Path(src: Path?)
```

Create a new path, copying the contents from the src path.

| Parameters ||
|---|---|
| `src` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path#)?: The path to copy from when initializing the new path. This value may be `null`. |

## Public methods

### addArc

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addArc(
    oval: RectF, 
    startAngle: Float, 
    sweepAngle: Float
): Unit
```

Add the specified arc to the path as a new contour.

| Parameters ||
|---|---|
| `oval` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF): The bounds of oval defining the shape and size of the arc. This value cannot be `null`. |
| `startAngle` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Starting angle (in degrees) where the arc begins |
| `sweepAngle` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Sweep angle (in degrees) measured clockwise |
| --- | --- |

### addArc

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addArc(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float, 
    startAngle: Float, 
    sweepAngle: Float
): Unit
```

Add the specified arc to the path as a new contour.

| Parameters ||
|---|---|
| `startAngle` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Starting angle (in degrees) where the arc begins |
| `sweepAngle` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Sweep angle (in degrees) measured clockwise |

### addCircle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addCircle(
    x: Float, 
    y: Float, 
    radius: Float, 
    dir: Path.Direction
): Unit
```

Add a closed circle contour to the path

| Parameters ||
|---|---|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The x-coordinate of the center of a circle to add to the path |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The y-coordinate of the center of a circle to add to the path |
| `radius` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The radius of a circle to add to the path |
| --- | --- |
| `dir` | [Path.Direction](https://developer.android.com/reference/kotlin/android/graphics/Path.Direction): The direction to wind the circle's contour. This value cannot be `null`. |

### addOval

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addOval(
    oval: RectF, 
    dir: Path.Direction
): Unit
```

Add a closed oval contour to the path

| Parameters ||
|---|---|
| `oval` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF): The bounds of the oval to add as a closed contour to the path. This value cannot be `null`. |
| `dir` | [Path.Direction](https://developer.android.com/reference/kotlin/android/graphics/Path.Direction): The direction to wind the oval's contour. This value cannot be `null`. |

### addOval

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addOval(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float, 
    dir: Path.Direction
): Unit
```

Add a closed oval contour to the path

| Parameters ||
|---|---|
| `dir` | [Path.Direction](https://developer.android.com/reference/kotlin/android/graphics/Path.Direction): The direction to wind the oval's contour. This value cannot be `null`. |

### addPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addPath(src: Path): Unit
```

Add a copy of src to the path

| Parameters ||
|---|---|
| `src` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path#): The path that is appended to the current path. This value cannot be `null`. |

### addPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addPath(
    src: Path, 
    matrix: Matrix
): Unit
```

Add a copy of src to the path, transformed by matrix

| Parameters ||
|---|---|
| `src` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path#): The path to add as a new contour. This value cannot be `null`. |
| `matrix` | [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix): This value cannot be `null`. |

### addPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addPath(
    src: Path, 
    dx: Float, 
    dy: Float
): Unit
```

Add a copy of src to the path, offset by (dx,dy)

| Parameters ||
|---|---|
| `src` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path#): The path to add as a new contour. This value cannot be `null`. |
| `dx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The amount to translate the path in X as it is added |

### addRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addRect(
    rect: RectF, 
    dir: Path.Direction
): Unit
```

Add a closed rectangle contour to the path

| Parameters ||
|---|---|
| `rect` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF): The rectangle to add as a closed contour to the path. This value cannot be `null`. |
| `dir` | [Path.Direction](https://developer.android.com/reference/kotlin/android/graphics/Path.Direction): The direction to wind the rectangle's contour. This value cannot be `null`. |

### addRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addRect(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float, 
    dir: Path.Direction
): Unit
```

Add a closed rectangle contour to the path

| Parameters ||
|---|---|
| `left` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The left side of a rectangle to add to the path |
| `top` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The top of a rectangle to add to the path |
| `right` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The right side of a rectangle to add to the path |
| --- | --- |
| `bottom` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The bottom of a rectangle to add to the path |
| `dir` | [Path.Direction](https://developer.android.com/reference/kotlin/android/graphics/Path.Direction): The direction to wind the rectangle's contour. This value cannot be `null`. |

### addRoundRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addRoundRect(
    rect: RectF, 
    rx: Float, 
    ry: Float, 
    dir: Path.Direction
): Unit
```

Add a closed round-rectangle contour to the path

| Parameters ||
|---|---|
| `rect` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF): The bounds of a round-rectangle to add to the path. This value cannot be `null`. |
| `rx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The x-radius of the rounded corners on the round-rectangle |
| `ry` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The y-radius of the rounded corners on the round-rectangle |
| --- | --- |
| `dir` | [Path.Direction](https://developer.android.com/reference/kotlin/android/graphics/Path.Direction): The direction to wind the round-rectangle's contour. This value cannot be `null`. |

### addRoundRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addRoundRect(
    rect: RectF, 
    radii: FloatArray, 
    dir: Path.Direction
): Unit
```

Add a closed round-rectangle contour to the path. Each corner receives two radius values \[X, Y\]. The corners are ordered top-left, top-right, bottom-right, bottom-left

| Parameters ||
|---|---|
| `rect` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF): The bounds of a round-rectangle to add to the path. This value cannot be `null`. |
| `radii` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): Array of 8 values, 4 pairs of \[X,Y\] radii. This value cannot be `null`. |
| `dir` | [Path.Direction](https://developer.android.com/reference/kotlin/android/graphics/Path.Direction): The direction to wind the round-rectangle's contour. This value cannot be `null`. |
| --- | --- |

### addRoundRect

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addRoundRect(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float, 
    rx: Float, 
    ry: Float, 
    dir: Path.Direction
): Unit
```

Add a closed round-rectangle contour to the path

| Parameters ||
|---|---|
| `rx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The x-radius of the rounded corners on the round-rectangle |
| `ry` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The y-radius of the rounded corners on the round-rectangle |
| `dir` | [Path.Direction](https://developer.android.com/reference/kotlin/android/graphics/Path.Direction): The direction to wind the round-rectangle's contour. This value cannot be `null`. |
| --- | --- |

### addRoundRect

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addRoundRect(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float, 
    radii: FloatArray, 
    dir: Path.Direction
): Unit
```

Add a closed round-rectangle contour to the path. Each corner receives two radius values \[X, Y\]. The corners are ordered top-left, top-right, bottom-right, bottom-left

| Parameters ||
|---|---|
| `radii` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): Array of 8 values, 4 pairs of \[X,Y\] radii. This value cannot be `null`. |
| `dir` | [Path.Direction](https://developer.android.com/reference/kotlin/android/graphics/Path.Direction): The direction to wind the round-rectangle's contour. This value cannot be `null`. |

### approximate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun approximate(acceptableError: Float): FloatArray
```

Approximate the `Path` with a series of line segments. This returns float\[\] with the array containing point components. There are three components for each point, in order:

- Fraction along the length of the path that the point resides
- The x coordinate of the point
- The y coordinate of the point

<br />

Two points may share the same fraction along its length when there is a move action within the Path.

| Parameters ||
|---|---|
| `acceptableError` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The acceptable error for a line on the Path. Typically this would be 0.5 so that the error is less than half a pixel. Value is 0.0f or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html` | An array of components for points approximating the Path. This value cannot be `null`. |

### arcTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun arcTo(
    oval: RectF, 
    startAngle: Float, 
    sweepAngle: Float
): Unit
```

Append the specified arc to the path as a new contour. If the start of the path is different from the path's current last point, then an automatic lineTo() is added to connect the current contour to the start of the arc. However, if the path is empty, then we call moveTo() with the first point of the arc.

| Parameters ||
|---|---|
| `oval` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF): The bounds of oval defining shape and size of the arc. This value cannot be `null`. |
| `startAngle` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Starting angle (in degrees) where the arc begins |
| `sweepAngle` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Sweep angle (in degrees) measured clockwise |
| --- | --- |

### arcTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun arcTo(
    oval: RectF, 
    startAngle: Float, 
    sweepAngle: Float, 
    forceMoveTo: Boolean
): Unit
```

Append the specified arc to the path as a new contour. If the start of the path is different from the path's current last point, then an automatic lineTo() is added to connect the current contour to the start of the arc. However, if the path is empty, then we call moveTo() with the first point of the arc.

| Parameters ||
|---|---|
| `oval` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF): The bounds of oval defining shape and size of the arc. This value cannot be `null`. |
| `startAngle` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Starting angle (in degrees) where the arc begins |
| `sweepAngle` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Sweep angle (in degrees) measured clockwise, treated mod 360. |
| --- | --- |
| `forceMoveTo` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, always begin a new contour with the arc |

### arcTo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun arcTo(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float, 
    startAngle: Float, 
    sweepAngle: Float, 
    forceMoveTo: Boolean
): Unit
```

Append the specified arc to the path as a new contour. If the start of the path is different from the path's current last point, then an automatic lineTo() is added to connect the current contour to the start of the arc. However, if the path is empty, then we call moveTo() with the first point of the arc.

| Parameters ||
|---|---|
| `startAngle` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Starting angle (in degrees) where the arc begins |
| `sweepAngle` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Sweep angle (in degrees) measured clockwise, treated mod 360. |
| `forceMoveTo` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, always begin a new contour with the arc |
| --- | --- |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun close(): Unit
```

Close the current contour. If the current point is not equal to the first point of the contour, a line segment is automatically added.

### computeBounds

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun computeBounds(bounds: RectF): Unit
```

Compute the bounds of the control points of the path, and write the answer into bounds. If the path contains 0 or 1 points, the bounds is set to (0,0,0,0)

| Parameters ||
|---|---|
| `bounds` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF): Returns the computed bounds of the path's control points. This value cannot be `null`. |

### computeBounds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun computeBounds(
    bounds: RectF, 
    exact: Boolean
): Unit
```

Compute the bounds of the control points of the path, and write the answer into bounds. If the path contains 0 or 1 points, the bounds is set to (0,0,0,0)

| Parameters ||
|---|---|
| `bounds` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF): Returns the computed bounds of the path's control points. This value cannot be `null`. |
| `exact` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): This parameter is no longer used. |

### conicTo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun conicTo(
    x1: Float, 
    y1: Float, 
    x2: Float, 
    y2: Float, 
    weight: Float
): Unit
```

Add a quadratic bezier from the last point, approaching control point (x1,y1), and ending at (x2,y2), weighted by `weight`. If no moveTo() call has been made for this contour, the first point is automatically set to (0,0). A weight of 1 is equivalent to calling `https://developer.android.com/reference/kotlin/android/graphics/Path#quadTo(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float)`. A weight of 0 is equivalent to calling `https://developer.android.com/reference/kotlin/android/graphics/Path#lineTo(kotlin.Float,%20kotlin.Float)` to `(x1, y1)` followed by `https://developer.android.com/reference/kotlin/android/graphics/Path#lineTo(kotlin.Float,%20kotlin.Float)` to `(x2, y2)`.

| Parameters ||
|---|---|
| `x1` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The x-coordinate of the control point on a conic curve |
| `y1` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The y-coordinate of the control point on a conic curve |
| `x2` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The x-coordinate of the end point on a conic curve |
| --- | --- |
| `y2` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The y-coordinate of the end point on a conic curve |
| `weight` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The weight of the conic applied to the curve. A value of 1 is equivalent to a quadratic with the given control and anchor points and a value of 0 is equivalent to a line to the first and another line to the second point. |

### cubicTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cubicTo(
    x1: Float, 
    y1: Float, 
    x2: Float, 
    y2: Float, 
    x3: Float, 
    y3: Float
): Unit
```

Add a cubic bezier from the last point, approaching control points (x1,y1) and (x2,y2), and ending at (x3,y3). If no moveTo() call has been made for this contour, the first point is automatically set to (0,0).

| Parameters ||
|---|---|
| `x1` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The x-coordinate of the 1st control point on a cubic curve |
| `y1` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The y-coordinate of the 1st control point on a cubic curve |
| `x2` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The x-coordinate of the 2nd control point on a cubic curve |
| --- | --- |
| `y2` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The y-coordinate of the 2nd control point on a cubic curve |
| `x3` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The x-coordinate of the end point on a cubic curve |
| `y3` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The y-coordinate of the end point on a cubic curve |
| --- | --- |

### getFillType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFillType(): Path.FillType
```

Return the path's fill type. This defines how "inside" is computed. The default value is WINDING.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Path.FillType` | the path's fill type. This value cannot be `null`. |

### getGenerationId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGenerationId(): Int
```

Returns the generation ID of this path. The generation ID changes whenever the path is modified. This can be used as an efficient way to check if a path has changed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The current generation ID for this path |

### getPathIterator

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPathIterator(): PathIterator
```

Returns an iterator over the segments of this path.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/PathIterator` | the Iterator object. This value cannot be `null`. |

### incReserve

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun incReserve(extraPtCount: Int): Unit
```

Hint to the path to prepare for adding more points. This can allow the path to more efficiently allocate its storage.

| Parameters ||
|---|---|
| `extraPtCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of extra points that may be added to this path |

### interpolate

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun interpolate(
    otherPath: Path, 
    t: Float, 
    interpolatedPath: Path
): Boolean
```

This method will linearly interpolate from this path to `otherPath` given the interpolation parameter `t`, returning the result in `interpolatedPath`. Interpolation will only succeed if the structures of the two paths match exactly, as discussed in `https://developer.android.com/reference/kotlin/android/graphics/Path#isInterpolatable(android.graphics.Path)`.

| Parameters ||
|---|---|
| `otherPath` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path#): The other `Path` being interpolated to. This value cannot be `null`. |
| `t` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The interpolation parameter. A value of 1 results in a `Path` equivalent to this path, a value of 0 results in one equivalent to `otherPath`. |
| `interpolatedPath` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path#): The interpolated results. This value cannot be `null`. |
| --- | --- |

### isConvex

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isConvex(): Boolean
```

**Deprecated:** *This method is not reliable. The way convexity is computed may change from release to release, and convexity could change based on a matrix as well. This method was useful when non-convex Paths were unable to be used in certain contexts, but that is no longer the case.*

Returns the path's convexity, as defined by the content of the path.

A path is convex if it has a single contour, and only ever curves in a single direction.

This function will calculate the convexity of the path from its control points, and cache the result.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the path is convex. |

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isEmpty(): Boolean
```

Returns true if the path is empty (contains no lines or curves)

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the path is empty (contains no lines or curves) |

### isInterpolatable

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isInterpolatable(otherPath: Path): Boolean
```

Two paths can be interpolated, by calling `https://developer.android.com/reference/kotlin/android/graphics/Path#interpolate(android.graphics.Path,%20kotlin.Float,%20android.graphics.Path)`, if they have exactly the same structure. That is, both paths must have the same operations, in the same order. If any of the operations are of type `https://developer.android.com/reference/kotlin/android/graphics/PathIterator#VERB_CONIC:kotlin.Int`, then the weights of those conics must also match.

| Parameters ||
|---|---|
| `otherPath` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path#): The other `Path` being interpolated to from this one. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if interpolation is possible, false otherwise |

### isInverseFillType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isInverseFillType(): Boolean
```

Returns true if the filltype is one of the INVERSE variants

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the filltype is one of the INVERSE variants |

### isRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isRect(rect: RectF?): Boolean
```

Returns true if the path specifies a rectangle. If so, and if rect is not null, set rect to the bounds of the path. If the path does not specify a rectangle, return false and ignore rect.

| Parameters ||
|---|---|
| `rect` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)?: If not null, returns the bounds of the path if it specifies a rectangle |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the path specifies a rectangle |

### lineTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun lineTo(
    x: Float, 
    y: Float
): Unit
```

Add a line from the last point to the specified point (x,y). If no moveTo() call has been made for this contour, the first point is automatically set to (0,0).

| Parameters ||
|---|---|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The x-coordinate of the end of a line |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The y-coordinate of the end of a line |

### moveTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun moveTo(
    x: Float, 
    y: Float
): Unit
```

Set the beginning of the next contour to the point (x,y).

| Parameters ||
|---|---|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The x-coordinate of the start of a new contour |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The y-coordinate of the start of a new contour |

### offset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun offset(
    dx: Float, 
    dy: Float
): Unit
```

Offset the path by (dx,dy)

| Parameters ||
|---|---|
| `dx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The amount in the X direction to offset the entire path |
| `dy` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The amount in the Y direction to offset the entire path |

### offset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun offset(
    dx: Float, 
    dy: Float, 
    dst: Path?
): Unit
```

Offset the path by (dx,dy)

| Parameters ||
|---|---|
| `dx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The amount in the X direction to offset the entire path |
| `dy` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The amount in the Y direction to offset the entire path |
| `dst` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path#)?: The translated path is written here. If this is null, then the original path is modified. |
| --- | --- |

### op

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun op(
    path1: Path, 
    path2: Path, 
    op: Path.Op
): Boolean
```

Set this path to the result of applying the Op to the two specified paths. The resulting path will be constructed from non-overlapping contours. The curve order is reduced where possible so that cubics may be turned into quadratics, and quadratics maybe turned into lines.

| Parameters ||
|---|---|
| `path1` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path#): The first operand (for difference, the minuend). This value cannot be `null`. |
| `path2` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path#): The second operand (for difference, the subtrahend). This value cannot be `null`. |
| `op` | [Path.Op](https://developer.android.com/reference/kotlin/android/graphics/Path.Op): This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if operation succeeded, false otherwise and this path remains unmodified. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Path.Op`
- `https://developer.android.com/reference/kotlin/android/graphics/Path#op(android.graphics.Path,%20android.graphics.Path.Op)`

### op

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun op(
    path: Path, 
    op: Path.Op
): Boolean
```

Set this path to the result of applying the Op to this path and the specified path. The resulting path will be constructed from non-overlapping contours. The curve order is reduced where possible so that cubics may be turned into quadratics, and quadratics maybe turned into lines.

| Parameters ||
|---|---|
| `path` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path#): The second operand (for difference, the subtrahend). This value cannot be `null`. |
| `op` | [Path.Op](https://developer.android.com/reference/kotlin/android/graphics/Path.Op): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if operation succeeded, false otherwise and this path remains unmodified. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Path.Op`
- `https://developer.android.com/reference/kotlin/android/graphics/Path#op(android.graphics.Path,%20android.graphics.Path,%20android.graphics.Path.Op)`

### quadTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun quadTo(
    x1: Float, 
    y1: Float, 
    x2: Float, 
    y2: Float
): Unit
```

Add a quadratic bezier from the last point, approaching control point (x1,y1), and ending at (x2,y2). If no moveTo() call has been made for this contour, the first point is automatically set to (0,0).

| Parameters ||
|---|---|
| `x1` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The x-coordinate of the control point on a quadratic curve |
| `y1` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The y-coordinate of the control point on a quadratic curve |
| `x2` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The x-coordinate of the end point on a quadratic curve |
| --- | --- |
| `y2` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The y-coordinate of the end point on a quadratic curve |

### rConicTo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun rConicTo(
    dx1: Float, 
    dy1: Float, 
    dx2: Float, 
    dy2: Float, 
    weight: Float
): Unit
```

Same as conicTo, but the coordinates are considered relative to the last point on this contour. If there is no previous point, then a moveTo(0,0) is inserted automatically.

| Parameters ||
|---|---|
| `dx1` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The amount to add to the x-coordinate of the last point on this contour, for the control point of a conic curve |
| `dy1` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The amount to add to the y-coordinate of the last point on this contour, for the control point of a conic curve |
| `dx2` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The amount to add to the x-coordinate of the last point on this contour, for the end point of a conic curve |
| --- | --- |
| `dy2` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The amount to add to the y-coordinate of the last point on this contour, for the end point of a conic curve |
| `weight` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The weight of the conic applied to the curve. A value of 1 is equivalent to a quadratic with the given control and anchor points and a value of 0 is equivalent to a line to the first and another line to the second point. |

### rCubicTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun rCubicTo(
    x1: Float, 
    y1: Float, 
    x2: Float, 
    y2: Float, 
    x3: Float, 
    y3: Float
): Unit
```

Same as cubicTo, but the coordinates are considered relative to the current point on this contour. If there is no previous point, then a moveTo(0,0) is inserted automatically.

### rLineTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun rLineTo(
    dx: Float, 
    dy: Float
): Unit
```

Same as lineTo, but the coordinates are considered relative to the last point on this contour. If there is no previous point, then a moveTo(0,0) is inserted automatically.

| Parameters ||
|---|---|
| `dx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The amount to add to the x-coordinate of the previous point on this contour, to specify a line |
| `dy` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The amount to add to the y-coordinate of the previous point on this contour, to specify a line |

### rMoveTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun rMoveTo(
    dx: Float, 
    dy: Float
): Unit
```

Set the beginning of the next contour relative to the last point on the previous contour. If there is no previous contour, this is treated the same as moveTo().

| Parameters ||
|---|---|
| `dx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The amount to add to the x-coordinate of the end of the previous contour, to specify the start of a new contour |
| `dy` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The amount to add to the y-coordinate of the end of the previous contour, to specify the start of a new contour |

### rQuadTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun rQuadTo(
    dx1: Float, 
    dy1: Float, 
    dx2: Float, 
    dy2: Float
): Unit
```

Same as quadTo, but the coordinates are considered relative to the last point on this contour. If there is no previous point, then a moveTo(0,0) is inserted automatically.

| Parameters ||
|---|---|
| `dx1` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The amount to add to the x-coordinate of the last point on this contour, for the control point of a quadratic curve |
| `dy1` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The amount to add to the y-coordinate of the last point on this contour, for the control point of a quadratic curve |
| `dx2` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The amount to add to the x-coordinate of the last point on this contour, for the end point of a quadratic curve |
| --- | --- |
| `dy2` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The amount to add to the y-coordinate of the last point on this contour, for the end point of a quadratic curve |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reset(): Unit
```

Clear any lines and curves from the path, making it empty. This does NOT change the fill-type setting.

### rewind

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun rewind(): Unit
```

Rewinds the path: clears any lines and curves from the path but keeps the internal data structure for faster reuse.

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun set(src: Path): Unit
```

Replace the contents of this with the contents of src.

| Parameters ||
|---|---|
| `src` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path#): This value cannot be `null`. |

### setFillType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFillType(ft: Path.FillType): Unit
```

Set the path's fill type. This defines how "inside" is computed.

| Parameters ||
|---|---|
| `ft` | [Path.FillType](https://developer.android.com/reference/kotlin/android/graphics/Path.FillType): The new fill type for this path. This value cannot be `null`. |

### setLastPoint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLastPoint(
    dx: Float, 
    dy: Float
): Unit
```

Sets the last point of the path.

| Parameters ||
|---|---|
| `dx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The new X coordinate for the last point |
| `dy` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The new Y coordinate for the last point |

### toggleInverseFillType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toggleInverseFillType(): Unit
```

Toggles the INVERSE state of the filltype

### transform

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun transform(matrix: Matrix): Unit
```

Transform the points in this path by matrix.

| Parameters ||
|---|---|
| `matrix` | [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix): The matrix to apply to the path. This value cannot be `null`. |

### transform

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun transform(
    matrix: Matrix, 
    dst: Path?
): Unit
```

Transform the points in this path by matrix, and write the answer into dst. If dst is null, then the the original path is modified.

| Parameters ||
|---|---|
| `matrix` | [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix): The matrix to apply to the path. This value cannot be `null`. |
| `dst` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path#)?: The transformed path is written here. If dst is null, then the the original path is modified |
