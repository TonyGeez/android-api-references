Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RenderNode

```
class RenderNode
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.RenderNode](https://developer.android.com/reference/kotlin/android/graphics/RenderNode#) |

RenderNode is used to build hardware accelerated rendering hierarchies. Each RenderNode contains both a display list as well as a set of properties that affect the rendering of the display list. RenderNodes are used internally for all Views by default and are not typically used directly.

RenderNodes are used to divide up the rendering content of a complex scene into smaller pieces that can then be updated individually more cheaply. Updating part of the scene only needs to update the display list or properties of a small number of RenderNode instead of redrawing everything from scratch. A RenderNode only needs its display list re-recorded when its content alone should be changed. RenderNodes can also be transformed without re-recording the display list through the transform properties.

A text editor might for instance store each paragraph into its own RenderNode. Thus when the user inserts or removes characters, only the display list of the affected paragraph needs to be recorded again.

### Hardware acceleration

RenderNodes can be drawn using a `https://developer.android.com/reference/kotlin/android/graphics/RecordingCanvas`. They are not supported in software. Always make sure that the `https://developer.android.com/reference/kotlin/android/graphics/Canvas` you are using to render a display list is hardware accelerated using `https://developer.android.com/reference/kotlin/android/graphics/Canvas#isHardwareAccelerated()`.

### Creating a RenderNode

```kotlin
RenderNode renderNode = new RenderNode("myRenderNode");
      renderNode.setPosition(0, 0, 50, 50); // Set the size to 50x50
      RecordingCanvas canvas = renderNode.beginRecording();
      try {
          // Draw with the canvas
          canvas.drawRect(...);
      } finally {
          renderNode.endRecording();
      }
```

### Drawing a RenderNode in a View

```kotlin
protected void onDraw(Canvas canvas) {
          if (canvas.isHardwareAccelerated()) {
              // Check that the RenderNode has a display list, re-recording it if it does not.
              if (!myRenderNode.hasDisplayList()) {
                  updateDisplayList(myRenderNode);
              }
              // Draw the RenderNode into this canvas.
              canvas.drawRenderNode(myRenderNode);
          }
      }
```

### Releasing resources

This step is not mandatory but recommended if you want to release resources held by a display list as soon as possible. Most significantly any bitmaps it may contain.

```kotlin
// Discards the display list content allowing for any held resources to be released.
      // After calling this
      renderNode.discardDisplayList();
```

### Properties

In addition, a RenderNode offers several properties, such as `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setScaleX(kotlin.Float)` or `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setTranslationX(kotlin.Float)`, that can be used to affect all the drawing commands recorded within. For instance, these properties can be used to move around a large number of images without re-issuing all the individual `canvas.drawBitmap()` calls.

```kotlin
private void createDisplayList() {
          mRenderNode = new RenderNode("MyRenderNode");
          mRenderNode.setPosition(0, 0, width, height);
          RecordingCanvas canvas = mRenderNode.beginRecording();
          try {
              for (Bitmap b : mBitmaps) {
                  canvas.drawBitmap(b, 0.0f, 0.0f, null);
                  canvas.translate(0.0f, b.getHeight());
              }
          } finally {
              mRenderNode.endRecording();
          }
      }
 
      protected void onDraw(Canvas canvas) {
          if (canvas.isHardwareAccelerated())
              canvas.drawRenderNode(mRenderNode);
          }
      }
 
      private void moveContentBy(int x) {
           // This will move all the bitmaps recorded inside the display list
           // by x pixels to the right and redraw this view. All the commands
           // recorded in createDisplayList() won't be re-issued, only onDraw()
           // will be invoked and will execute very quickly
           mRenderNode.offsetLeftAndRight(x);
           invalidate();
      }
```

A few of the properties may at first appear redundant, such as `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setElevation(kotlin.Float)` and `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setTranslationZ(kotlin.Float)`. The reason for these duplicates are to allow for a separation between static \& transient usages. For example consider a button that raises from 2dp to 8dp when pressed. To achieve that an application may decide to setElevation(2dip), and then on press to animate setTranslationZ to 6dip. Combined this achieves the final desired 8dip value, but the animation need only concern itself with animating the lift from press without needing to know the initial starting value. `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setTranslationX(kotlin.Float)` and `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setTranslationY(kotlin.Float)` are similarly provided for animation uses despite the functional overlap with `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setPosition(android.graphics.Rect)`.

The RenderNode's transform matrix is computed at render time as follows:

```kotlin
Matrix transform = new Matrix();
      transform.setTranslate(renderNode.getTranslationX(), renderNode.getTranslationY());
      transform.preRotate(renderNode.getRotationZ(),
              renderNode.getPivotX(), renderNode.getPivotY());
      transform.preScale(renderNode.getScaleX(), renderNode.getScaleY(),
              renderNode.getPivotX(), renderNode.getPivotY());
```
The current canvas transform matrix, which is translated to the RenderNode's position, is then multiplied by the RenderNode's transform matrix. Therefore the ordering of calling property setters does not affect the result. That is to say that:

```kotlin
renderNode.setTranslationX(100);
      renderNode.setScaleX(100);
```
is equivalent to:

```kotlin
renderNode.setScaleX(100);
      renderNode.setTranslationX(100);
```

### Threading

RenderNode may be created and used on any thread but they are not thread-safe. Only a single thread may interact with a RenderNode at any given time. It is critical that the RenderNode is only used on the same thread it is drawn with. For example when using RenderNode with a custom View, then that RenderNode must only be used from the UI thread.

### When to re-render

Many of the RenderNode mutation methods, such as `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setTranslationX(kotlin.Float)`, return a boolean indicating if the value actually changed or not. This is useful in detecting if a new frame should be rendered or not. A typical usage would look like:

```kotlin
public void translateTo(int x, int y) {
          boolean needsUpdate = myRenderNode.setTranslationX(x);
          needsUpdate |= myRenderNode.setTranslationY(y);
          if (needsUpdate) {
              myOwningView.invalidate();
          }
      }
```
This is marginally faster than doing a more explicit up-front check if the value changed by comparing the desired value against `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getTranslationX()` as it minimizes JNI transitions. The actual mechanism of requesting a new frame to be rendered will depend on how this RenderNode is being drawn. If it's drawn to a containing View, as in the above snippet, then simply invalidating that View works. If instead the RenderNode is being drawn to a Canvas directly such as with `https://developer.android.com/reference/kotlin/android/view/Surface.html#lockHardwareCanvas()` then a new frame needs to be drawn by calling `https://developer.android.com/reference/kotlin/android/view/Surface.html#lockHardwareCanvas()`, re-drawing the root RenderNode or whatever top-level content is desired, and finally calling `https://developer.android.com/reference/kotlin/android/view/Surface.html#unlockCanvasAndPost(android.graphics.Canvas)`.

<br />

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#RenderNode(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Creates a new RenderNode that can be used to record batches of drawing operations, and store / apply render properties when drawn. |

| Public methods ||
|---|---|
| [RecordingCanvas](https://developer.android.com/reference/kotlin/android/graphics/RecordingCanvas) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#beginRecording()()` Same as `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#beginRecording(kotlin.Int,%20kotlin.Int)` with the width \& height set to the RenderNode's own width \& height. |
| [RecordingCanvas](https://developer.android.com/reference/kotlin/android/graphics/RecordingCanvas) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#beginRecording(kotlin.Int,%20kotlin.Int)(width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Starts recording a display list for the render node. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#computeApproximateMemoryUsage()()` Gets the approximate memory usage of the RenderNode for debug purposes. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#discardDisplayList()()` Reset native resources. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#endRecording()()` \` Ends the recording for this display list. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getAlpha()()` Returns the translucency level of this display list. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getAmbientShadowColor()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getBottom()()` Gets the bottom position for the RenderNode. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getCameraDistance()()` Returns the distance in Z of the camera for this RenderNode |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getClipToBounds()()` Returns whether or not the RenderNode is clipping to its bounds. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getClipToOutline()()` See `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setClipToOutline(kotlin.Boolean)` |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getElevation()()` See `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setElevation(kotlin.Float)` |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getHeight()()` Gets the height of the RenderNode, which is the bottom - top. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getInverseMatrix(android.graphics.Matrix)(outMatrix: https://developer.android.com/reference/kotlin/android/graphics/Matrix)` Gets the current transform inverted. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getLeft()()` Gets the left position for the RenderNode. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getMatrix(android.graphics.Matrix)(outMatrix: https://developer.android.com/reference/kotlin/android/graphics/Matrix)` Gets the current transform matrix |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getPivotX()()` Returns the pivot value for this display list on the X axis, in pixels. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getPivotY()()` Returns the pivot value for this display list on the Y axis, in pixels. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getRight()()` Gets the right position for the RenderNode. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getRotationX()()` Returns the rotation value for this display list around the X axis, in degrees. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getRotationY()()` Returns the rotation value for this display list around the Y axis, in degrees. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getRotationZ()()` Returns the rotation value for this display list around the Z axis, in degrees. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getScaleX()()` Returns the scale value for this display list on the X axis. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getScaleY()()` Returns the scale value for this display list on the Y axis. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getSpotShadowColor()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getTop()()` Gets the top position for the RenderNode. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getTranslationX()()` Returns the translation value for this display list on the X axis, in pixels. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getTranslationY()()` Returns the translation value for this display list on the Y axis, in pixels. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getTranslationZ()()` Returns the translation value for this display list on the Z axis. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getUniqueId()()` Returns the unique ID that identifies this RenderNode. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getUseCompositingLayer()()` Gets whether or not a compositing layer is forced to be used. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getWidth()()` Gets the width of the RenderNode, which is the right - left. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#hasDisplayList()()` Returns whether the RenderNode has a display list. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#hasIdentityMatrix()()` Whether or not the RenderNode has an identity transform. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#hasOverlappingRendering()()` Indicates whether the content of this display list overlaps. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#hasShadow()()` Checks if the RenderNode has a shadow. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#isForceDarkAllowed()()` See `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setForceDarkAllowed(kotlin.Boolean)` |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#isPivotExplicitlySet()()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#offsetLeftAndRight(kotlin.Int)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Offsets the left and right positions for the RenderNode |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#offsetTopAndBottom(kotlin.Int)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Offsets the top and bottom values for the RenderNode |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#resetPivot()()` Clears any pivot previously set by a call to `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setPivotX(kotlin.Float)` or `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setPivotY(kotlin.Float)`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setAlpha(kotlin.Float)(alpha: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the translucency level for the display list. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setAmbientShadowColor(kotlin.Int)(color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the color of the ambient shadow that is drawn when the RenderNode has a positive Z or elevation value and is drawn inside of a `https://developer.android.com/reference/kotlin/android/graphics/Canvas#enableZ()` section. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setBackdropRenderEffect(android.graphics.RenderEffect)(renderEffect: https://developer.android.com/reference/kotlin/android/graphics/RenderEffect?)` Configure the `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect` to apply to the backdrop contents of this RenderNode. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setCameraDistance(kotlin.Float)(distance: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the distance along the Z axis (orthogonal to the X/Y plane on which RenderNodes are drawn) from the camera to this RenderNode. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setClipRect(android.graphics.Rect)(rect: https://developer.android.com/reference/kotlin/android/graphics/Rect?)` Sets an additional clip on the RenderNode. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setClipToBounds(kotlin.Boolean)(clipToBounds: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set whether the Render node should clip itself to its bounds. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setClipToOutline(kotlin.Boolean)(clipToOutline: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Enables or disables clipping to the outline. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setElevation(kotlin.Float)(lift: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the base elevation of this RenderNode in pixels |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setForceDarkAllowed(kotlin.Boolean)(allow: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether or not to allow force dark to apply to this RenderNode. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setHasOverlappingRendering(kotlin.Boolean)(hasOverlappingRendering: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the display list renders content which overlaps. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setOutline(android.graphics.Outline)(outline: https://developer.android.com/reference/kotlin/android/graphics/Outline?)` Sets the outline, defining the shape that casts a shadow, and the path to be clipped if setClipToOutline is set. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setPivotX(kotlin.Float)(pivotX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the pivot value for the display list on the X axis |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setPivotY(kotlin.Float)(pivotY: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the pivot value for the display list on the Y axis |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setPosition(android.graphics.Rect)(position: https://developer.android.com/reference/kotlin/android/graphics/Rect)` Sets the position of the RenderNode. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setPosition(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the position of the RenderNode. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setProjectBackwards(kotlin.Boolean)(shouldProject: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the RenderNode should be drawn immediately after the closest ancestor RenderNode containing a projection receiver. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setProjectionReceiver(kotlin.Boolean)(shouldReceive: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the RenderNode is a projection receiver. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setRenderEffect(android.graphics.RenderEffect)(renderEffect: https://developer.android.com/reference/kotlin/android/graphics/RenderEffect?)` Configure the `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect` to apply to this RenderNode. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setRotationX(kotlin.Float)(rotationX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the rotation value for the display list around the X axis. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setRotationY(kotlin.Float)(rotationY: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the rotation value for the display list around the Y axis. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setRotationZ(kotlin.Float)(rotation: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the rotation value for the display list around the Z axis. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setScaleX(kotlin.Float)(scaleX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the scale value for the display list on the X axis. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setScaleY(kotlin.Float)(scaleY: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the scale value for the display list on the Y axis. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setSpotShadowColor(kotlin.Int)(color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the color of the spot shadow that is drawn when the RenderNode has a positive Z or elevation value and is drawn inside of a `https://developer.android.com/reference/kotlin/android/graphics/Canvas#enableZ()` section. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setTranslationX(kotlin.Float)(translationX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the translation value for the display list on the X axis. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setTranslationY(kotlin.Float)(translationY: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the translation value for the display list on the Y axis. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setTranslationZ(kotlin.Float)(translationZ: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the translation value for the display list on the Z axis. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setUseCompositingLayer(kotlin.Boolean,%20android.graphics.Paint)(forceToLayer: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, paint: https://developer.android.com/reference/kotlin/android/graphics/Paint?)` Controls whether or not to force this RenderNode to render to an intermediate buffer. |
| --- | --- |

## Public constructors

### RenderNode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RenderNode(name: String?)
```

Creates a new RenderNode that can be used to record batches of drawing operations, and store / apply render properties when drawn.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The name of the RenderNode, used for debugging purpose. May be null. |

## Public methods

### beginRecording

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun beginRecording(): RecordingCanvas
```

Same as `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#beginRecording(kotlin.Int,%20kotlin.Int)` with the width \& height set to the RenderNode's own width \& height. The RenderNode's width \& height may be set with `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setPosition(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/RecordingCanvas` | A canvas to record drawing operations. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If a recording is already in progress. That is, the previous call to `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#beginRecording(kotlin.Int,%20kotlin.Int)` did not call `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#endRecording()`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#endRecording()`
- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#hasDisplayList()`

### beginRecording

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun beginRecording(
    width: Int, 
    height: Int
): RecordingCanvas
```

Starts recording a display list for the render node. All operations performed on the returned canvas are recorded and stored in this display list. `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#endRecording()` must be called when the recording is finished in order to apply the updated display list. Failing to call `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#endRecording()` will result in an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` if `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#beginRecording(kotlin.Int,%20kotlin.Int)` is called again.

| Parameters ||
|---|---|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the recording viewport. This will not alter the width of the RenderNode itself, that must be set with `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setPosition(android.graphics.Rect)`. |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the recording viewport. This will not alter the height of the RenderNode itself, that must be set with `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setPosition(android.graphics.Rect)`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/RecordingCanvas` | A canvas to record drawing operations. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If a recording is already in progress. That is, the previous call to `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#beginRecording(kotlin.Int,%20kotlin.Int)` did not call `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#endRecording()`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#endRecording()`
- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#hasDisplayList()`

### computeApproximateMemoryUsage

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun computeApproximateMemoryUsage(): Long
```

Gets the approximate memory usage of the RenderNode for debug purposes. Does not include the memory usage of any child RenderNodes nor any bitmaps, only the memory usage of this RenderNode and any data it owns. 
Value is a non-negative number of bytes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Approximate memory usage in bytes. Value is a non-negative number of bytes. |

### discardDisplayList

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun discardDisplayList(): Unit
```

Reset native resources. This is called when cleaning up the state of display lists during destruction of hardware resources, to ensure that we do not hold onto obsolete resources after related resources are gone.

### endRecording

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun endRecording(): Unit
```

\` Ends the recording for this display list. Calling this method marks the display list valid and `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#hasDisplayList()` will return true.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#beginRecording(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#hasDisplayList()`

### getAlpha

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAlpha(): Float
```

Returns the translucency level of this display list.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | A value between 0.0f and 1.0f |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setAlpha(kotlin.Float)`

### getAmbientShadowColor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAmbientShadowColor(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The shadow color set by `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setAmbientShadowColor(kotlin.Int)`, or black if nothing was set |

### getBottom

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBottom(): Int
```

Gets the bottom position for the RenderNode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the bottom position in pixels |

### getCameraDistance

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCameraDistance(): Float
```

Returns the distance in Z of the camera for this RenderNode

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the distance along the Z axis in pixels. Value is between 0.0f and `https://developer.android.com/reference/kotlin/java/lang/Float.html#MAX_VALUE:kotlin.Float` inclusive |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setCameraDistance(kotlin.Float)`

### getClipToBounds

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getClipToBounds(): Boolean
```

Returns whether or not the RenderNode is clipping to its bounds. See `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setClipToBounds(kotlin.Boolean)` and `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setPosition(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the render node clips to its bounds, false otherwise. |

### getClipToOutline

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getClipToOutline(): Boolean
```

See `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setClipToOutline(kotlin.Boolean)`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if this RenderNode clips to its outline, false otherwise |

### getElevation

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getElevation(): Float
```

See `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setElevation(kotlin.Float)`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The RenderNode's current elevation |

### getHeight

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHeight(): Int
```

Gets the height of the RenderNode, which is the bottom - top.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the height of the RenderNode |

### getInverseMatrix

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInverseMatrix(outMatrix: Matrix): Unit
```

Gets the current transform inverted. This is a faster way to do the otherwise equivalent `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getMatrix(android.graphics.Matrix)` followed by `https://developer.android.com/reference/kotlin/android/graphics/Matrix#invert(android.graphics.Matrix)`

| Parameters ||
|---|---|
| `outMatrix` | [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix): The matrix to store the inverse transform of the RenderNode. This value cannot be `null`. |

### getLeft

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLeft(): Int
```

Gets the left position for the RenderNode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the left position in pixels |

### getMatrix

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMatrix(outMatrix: Matrix): Unit
```

Gets the current transform matrix

| Parameters ||
|---|---|
| `outMatrix` | [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix): The matrix to store the transform of the RenderNode. This value cannot be `null`. |

### getPivotX

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPivotX(): Float
```

Returns the pivot value for this display list on the X axis, in pixels.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setPivotX(kotlin.Float)`

### getPivotY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPivotY(): Float
```

Returns the pivot value for this display list on the Y axis, in pixels.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setPivotY(kotlin.Float)`

### getRight

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRight(): Int
```

Gets the right position for the RenderNode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the right position in pixels |

### getRotationX

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRotationX(): Float
```

Returns the rotation value for this display list around the X axis, in degrees.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setRotationX(kotlin.Float)`

### getRotationY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRotationY(): Float
```

Returns the rotation value for this display list around the Y axis, in degrees.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setRotationY(kotlin.Float)`

### getRotationZ

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRotationZ(): Float
```

Returns the rotation value for this display list around the Z axis, in degrees.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setRotationZ(kotlin.Float)`

### getScaleX

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getScaleX(): Float
```

Returns the scale value for this display list on the X axis.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setScaleX(kotlin.Float)`

### getScaleY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getScaleY(): Float
```

Returns the scale value for this display list on the Y axis.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setScaleY(kotlin.Float)`

### getSpotShadowColor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSpotShadowColor(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The shadow color set by `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setSpotShadowColor(kotlin.Int)`, or black if nothing was set |

### getTop

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTop(): Int
```

Gets the top position for the RenderNode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the top position in pixels |

### getTranslationX

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTranslationX(): Float
```

Returns the translation value for this display list on the X axis, in pixels.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setTranslationX(kotlin.Float)`

### getTranslationY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTranslationY(): Float
```

Returns the translation value for this display list on the Y axis, in pixels.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setTranslationY(kotlin.Float)`

### getTranslationZ

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTranslationZ(): Float
```

Returns the translation value for this display list on the Z axis.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setTranslationZ(kotlin.Float)`

### getUniqueId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUniqueId(): Long
```

Returns the unique ID that identifies this RenderNode. This ID is unique for the lifetime of the process. IDs are reset on process death, and are unique only within the process. This ID is intended to be used with debugging tools to associate a particular RenderNode across different debug dumping \& inspection tools. For example a View layout inspector should include the unique ID for any RenderNodes that it owns to associate the drawing content with the layout content.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the unique ID for this RenderNode |

### getUseCompositingLayer

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUseCompositingLayer(): Boolean
```

Gets whether or not a compositing layer is forced to be used. The default \& recommended is false, as it is typically faster to avoid using compositing layers. See `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setUseCompositingLayer(kotlin.Boolean,%20android.graphics.Paint)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if a compositing layer is forced, false otherwise |

### getWidth

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getWidth(): Int
```

Gets the width of the RenderNode, which is the right - left.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the width of the RenderNode |

### hasDisplayList

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasDisplayList(): Boolean
```

Returns whether the RenderNode has a display list. If this returns false, the RenderNode should be re-recorded with `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#beginRecording()` and `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#endRecording()`. A RenderNode without a display list may still be drawn, however it will have no impact on the rendering content until its display list is updated. When a RenderNode is no longer drawn by anything the system may automatically invoke `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#discardDisplayList()`. It is therefore important to ensure that `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#hasDisplayList()` is true on a RenderNode prior to drawing it. See `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#discardDisplayList()`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | boolean true if this RenderNode has a display list, false otherwise. |

### hasIdentityMatrix

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasIdentityMatrix(): Boolean
```

Whether or not the RenderNode has an identity transform. This is a faster way to do the otherwise equivalent `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getMatrix(android.graphics.Matrix)` `https://developer.android.com/reference/kotlin/android/graphics/Matrix#isIdentity()` as it doesn't require copying the Matrix first, thus minimizing overhead.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the RenderNode has an identity transform, false otherwise |

### hasOverlappingRendering

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasOverlappingRendering(): Boolean
```

Indicates whether the content of this display list overlaps.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if this display list renders content which overlaps, false otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setHasOverlappingRendering(kotlin.Boolean)`

### hasShadow

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasShadow(): Boolean
```

Checks if the RenderNode has a shadow. That is, if the combination of `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getElevation()` and `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getTranslationZ()` is greater than zero, there is an `https://developer.android.com/reference/kotlin/android/graphics/Outline` set with a valid shadow caster path, and the provided outline has a non-zero `https://developer.android.com/reference/kotlin/android/graphics/Outline#getAlpha()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if this RenderNode has a shadow, false otherwise |

### isForceDarkAllowed

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isForceDarkAllowed(): Boolean
```

See `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setForceDarkAllowed(kotlin.Boolean)`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if force dark is allowed (default), false if it is disabled |

### isPivotExplicitlySet

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isPivotExplicitlySet(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether or not a pivot was explicitly set with `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setPivotX(kotlin.Float)` or `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setPivotY(kotlin.Float)`. If no pivot has been set then the pivot will be the center of the RenderNode. |

### offsetLeftAndRight

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun offsetLeftAndRight(offset: Int): Boolean
```

Offsets the left and right positions for the RenderNode

| Parameters ||
|---|---|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The amount that the left and right positions are offset in pixels |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

### offsetTopAndBottom

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun offsetTopAndBottom(offset: Int): Boolean
```

Offsets the top and bottom values for the RenderNode

| Parameters ||
|---|---|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The amount that the left and right positions are offset in pixels |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

### resetPivot

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun resetPivot(): Boolean
```

Clears any pivot previously set by a call to `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setPivotX(kotlin.Float)` or `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setPivotY(kotlin.Float)`. After calling this `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#isPivotExplicitlySet()` will be false and the pivot used for rotation will return to default of being centered on the view.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

### setAlpha

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setAlpha(alpha: Float): Boolean
```

Sets the translucency level for the display list.

| Parameters ||
|---|---|
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The translucency of the display list, must be a value between 0.0f and 1.0f |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View.html#setAlpha(kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getAlpha()`

### setAmbientShadowColor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setAmbientShadowColor(color: Int): Boolean
```

Sets the color of the ambient shadow that is drawn when the RenderNode has a positive Z or elevation value and is drawn inside of a `https://developer.android.com/reference/kotlin/android/graphics/Canvas#enableZ()` section.

By default the shadow color is black. Generally, this color will be opaque so the intensity of the shadow is consistent between different RenderNodes with different colors.

The opacity of the final ambient shadow is a function of the shadow caster height, the alpha channel of the outlineAmbientShadowColor (typically opaque), and the `https://developer.android.com/reference/kotlin/android/R.attr.html#ambientShadowAlpha:kotlin.Int` theme attribute.

| Parameters ||
|---|---|
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The color this RenderNode will cast for its elevation shadow. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

### setBackdropRenderEffect

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setBackdropRenderEffect(renderEffect: RenderEffect?): Boolean
```

Configure the `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect` to apply to the backdrop contents of this RenderNode. This will apply a visual effect to the result of the backdrop contents of this RenderNode before the RenderNode is drawn into the destination. For example if `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#createBlurEffect(kotlin.Float,%20kotlin.Float,%20android.graphics.RenderEffect,%20android.graphics.Shader.TileMode)` is provided, the previous content behind this RenderNode will be blurred before the RenderNode is drawn in to the destination.

| Parameters ||
|---|---|
| `renderEffect` | [RenderEffect](https://developer.android.com/reference/kotlin/android/graphics/RenderEffect)?: to be applied to the backdrop contents of this RenderNode. Passing null clears all previously configured RenderEffects |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

### setCameraDistance

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setCameraDistance(distance: Float): Boolean
```

Sets the distance along the Z axis (orthogonal to the X/Y plane on which RenderNodes are drawn) from the camera to this RenderNode. The camera's distance affects 3D transformations, for instance rotations around the X and Y axis. If the rotationX or rotationY properties are changed and this view is large (more than half the size of the screen), it is recommended to always use a camera distance that's greater than the height (X axis rotation) or the width (Y axis rotation) of this view.

The distance of the camera from the drawing plane can have an affect on the perspective distortion of the RenderNode when it is rotated around the x or y axis. For example, a large distance will result in a large viewing angle, and there will not be much perspective distortion of the view as it rotates. A short distance may cause much more perspective distortion upon rotation, and can also result in some drawing artifacts if the rotated view ends up partially behind the camera (which is why the recommendation is to use a distance at least as far as the size of the view, if the view is to be rotated.)

The distance is expressed in pixels and must always be positive

| Parameters ||
|---|---|
| `distance` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The distance in pixels, must always be positive. Value is between 0.0f and `https://developer.android.com/reference/kotlin/java/lang/Float.html#MAX_VALUE:kotlin.Float` inclusive |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setRotationX(kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setRotationY(kotlin.Float)`

### setClipRect

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setClipRect(rect: Rect?): Boolean
```

Sets an additional clip on the RenderNode. If null, the extra clip is removed from the RenderNode. If non-null, the RenderNode will be clipped to this rect. In addition if `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setClipToBounds(kotlin.Boolean)` is true, then the RenderNode will be clipped to the intersection of this rectangle and the bounds of the render node, which is set with `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setPosition(android.graphics.Rect)`.

This is equivalent to do a `https://developer.android.com/reference/kotlin/android/graphics/Canvas#clipRect(android.graphics.Rect)` at the start of this RenderNode's display list. However, as this is a property of the RenderNode instead of part of the display list it can be more easily animated for transient additional clipping. An example usage of this would be the `https://developer.android.com/reference/kotlin/android/transition/ChangeBounds.html#` transition animation with the resizeClip=true option.

| Parameters ||
|---|---|
| `rect` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect)?: the bounds to clip to. If null, the additional clip is removed. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

### setClipToBounds

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setClipToBounds(clipToBounds: Boolean): Boolean
```

Set whether the Render node should clip itself to its bounds. This defaults to true, and is useful to the renderer in enable quick-rejection of chunks of the tree as well as better partial invalidation support. Clipping can be further restricted or controlled through the combination of this property as well as `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setClipRect(android.graphics.Rect)`, which allows for a different clipping rectangle to be used in addition to or instead of the `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setPosition(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` or the RenderNode.

| Parameters ||
|---|---|
| `clipToBounds` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the display list should clip to its bounds, false otherwise. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

### setClipToOutline

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setClipToOutline(clipToOutline: Boolean): Boolean
```

Enables or disables clipping to the outline.

| Parameters ||
|---|---|
| `clipToOutline` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if clipping to the outline. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the clipToOutline value changed, false if previous value matched the new value. |

### setElevation

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setElevation(lift: Float): Boolean
```

Sets the base elevation of this RenderNode in pixels

| Parameters ||
|---|---|
| `lift` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the elevation in pixels |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

### setForceDarkAllowed

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setForceDarkAllowed(allow: Boolean): Boolean
```

Sets whether or not to allow force dark to apply to this RenderNode. Setting this to false will disable the auto-dark feature on everything this RenderNode draws, including any descendants. Setting this to true will allow this RenderNode to be automatically made dark, however a value of 'true' will not override any 'false' value in its parent chain nor will it prevent any 'false' in any of its children.

| Parameters ||
|---|---|
| `allow` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether or not to allow force dark. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

### setHasOverlappingRendering

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setHasOverlappingRendering(hasOverlappingRendering: Boolean): Boolean
```

Sets whether the display list renders content which overlaps. Non-overlapping rendering can use a fast path for alpha that avoids rendering to an offscreen buffer. By default display lists consider they do not have overlapping content.

| Parameters ||
|---|---|
| `hasOverlappingRendering` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): False if the content is guaranteed to be non-overlapping, true otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View.html#hasOverlappingRendering()`
- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#hasOverlappingRendering()`

### setOutline

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setOutline(outline: Outline?): Boolean
```

Sets the outline, defining the shape that casts a shadow, and the path to be clipped if setClipToOutline is set. This will make a copy of the provided `https://developer.android.com/reference/kotlin/android/graphics/Outline`, so any future modifications to the outline will need to call `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setOutline(android.graphics.Outline)` with the modified outline for those changes to be applied.

| Parameters ||
|---|---|
| `outline` | [Outline](https://developer.android.com/reference/kotlin/android/graphics/Outline)?: The outline to use for this RenderNode. This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

### setPivotX

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPivotX(pivotX: Float): Boolean
```

Sets the pivot value for the display list on the X axis

| Parameters ||
|---|---|
| `pivotX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The pivot value of the display list on the X axis, in pixels |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View.html#setPivotX(kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getPivotX()`

### setPivotY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPivotY(pivotY: Float): Boolean
```

Sets the pivot value for the display list on the Y axis

| Parameters ||
|---|---|
| `pivotY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The pivot value of the display list on the Y axis, in pixels |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View.html#setPivotY(kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getPivotY()`

### setPosition

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPosition(position: Rect): Boolean
```

Sets the position of the RenderNode.

| Parameters ||
|---|---|
| `position` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect): The position rectangle in pixels. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

### setPosition

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPosition(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Boolean
```

Sets the position of the RenderNode.

| Parameters ||
|---|---|
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The left position of the RenderNode, in pixels |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The top position of the RenderNode, in pixels |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The right position of the RenderNode, in pixels |
| --- | --- |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The bottom position of the RenderNode, in pixels |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

### setProjectBackwards

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setProjectBackwards(shouldProject: Boolean): Boolean
```

Sets whether the RenderNode should be drawn immediately after the closest ancestor RenderNode containing a projection receiver.

The default is false, and the rendering of this node happens in the typical draw order.

If true, then at rendering time this rendernode will not be drawn in order with the `https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawRenderNode(android.graphics.RenderNode)` command that drew this RenderNode, but instead it will be re-positioned in the RenderNode tree to be drawn on the closet ancestor with a child rendernode that has `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setProjectionReceiver(kotlin.Boolean)` as true.

The typical usage of this is to allow a child RenderNode to draw on a parent's background, such as the platform's usage with `https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable`. Consider the following structure, built out of which RenderNode called drawRenderNode on a different RenderNode:

```kotlin
+---+
         |RenderNode: P|
         +-+---++
           |          |
           v          v
   +---+---+  +-+---+
   |RenderNode: C|  |RenderNode: P'BG|
   +---+---+  +---+
           |
           |
  +---+---+
  |RenderNode: C'BG|
  +---+
  
```
If P'BG is a projection receiver, and C'BG is set to project backwards then C'BG will behave as if it was drawn directly by P'BG instead of by C. This includes inheriting P'BG's clip instead of C's clip.

| Parameters ||
|---|---|
| `shouldProject` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the display list should be projected onto a containing volume. Default is false. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

### setProjectionReceiver

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setProjectionReceiver(shouldReceive: Boolean): Boolean
```

Sets whether the RenderNode is a projection receiver. If true then this RenderNode's parent should draw any descendant RenderNodes with ProjectBackwards=true directly on top of it. Default value is false. See `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setProjectBackwards(kotlin.Boolean)` for a description of what this entails.

| Parameters ||
|---|---|
| `shouldReceive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if this RenderNode is a projection receiver, false otherwise. Default is false. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

### setRenderEffect

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setRenderEffect(renderEffect: RenderEffect?): Boolean
```

Configure the `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect` to apply to this RenderNode. This will apply a visual effect to the end result of the contents of this RenderNode before it is drawn into the destination. For example if `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#createBlurEffect(kotlin.Float,%20kotlin.Float,%20android.graphics.RenderEffect,%20android.graphics.Shader.TileMode)` is provided, the contents will be drawn in a separate layer, then this layer will be blurred when this RenderNode is drawn into the destination.

| Parameters ||
|---|---|
| `renderEffect` | [RenderEffect](https://developer.android.com/reference/kotlin/android/graphics/RenderEffect)?: to be applied to the RenderNode. Passing null clears all previously configured RenderEffects |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

### setRotationX

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setRotationX(rotationX: Float): Boolean
```

Sets the rotation value for the display list around the X axis.

| Parameters ||
|---|---|
| `rotationX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The rotation value of the display list, in degrees |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View.html#setRotationX(kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getRotationX()`

### setRotationY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setRotationY(rotationY: Float): Boolean
```

Sets the rotation value for the display list around the Y axis.

| Parameters ||
|---|---|
| `rotationY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The rotation value of the display list, in degrees |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View.html#setRotationY(kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getRotationY()`

### setRotationZ

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setRotationZ(rotation: Float): Boolean
```

Sets the rotation value for the display list around the Z axis.

| Parameters ||
|---|---|
| `rotation` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The rotation value of the display list, in degrees |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View.html#setRotation(kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getRotationZ()`

### setScaleX

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setScaleX(scaleX: Float): Boolean
```

Sets the scale value for the display list on the X axis.

| Parameters ||
|---|---|
| `scaleX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scale value of the display list |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View.html#setScaleX(kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getScaleX()`

### setScaleY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setScaleY(scaleY: Float): Boolean
```

Sets the scale value for the display list on the Y axis.

| Parameters ||
|---|---|
| `scaleY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The scale value of the display list |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View.html#setScaleY(kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getScaleY()`

### setSpotShadowColor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setSpotShadowColor(color: Int): Boolean
```

Sets the color of the spot shadow that is drawn when the RenderNode has a positive Z or elevation value and is drawn inside of a `https://developer.android.com/reference/kotlin/android/graphics/Canvas#enableZ()` section.

By default the shadow color is black. Generally, this color will be opaque so the intensity of the shadow is consistent between different RenderNodes with different colors.

The opacity of the final spot shadow is a function of the shadow caster height, the alpha channel of the outlineSpotShadowColor (typically opaque), and the `https://developer.android.com/reference/kotlin/android/R.attr.html#spotShadowAlpha:kotlin.Int` theme attribute

| Parameters ||
|---|---|
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The color this RenderNode will cast for its elevation spot shadow. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

### setTranslationX

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setTranslationX(translationX: Float): Boolean
```

Sets the translation value for the display list on the X axis.

| Parameters ||
|---|---|
| `translationX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The X axis translation value of the display list, in pixels |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View.html#setTranslationX(kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getTranslationX()`

### setTranslationY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setTranslationY(translationY: Float): Boolean
```

Sets the translation value for the display list on the Y axis.

| Parameters ||
|---|---|
| `translationY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The Y axis translation value of the display list, in pixels |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View.html#setTranslationY(kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getTranslationY()`

### setTranslationZ

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setTranslationZ(translationZ: Float): Boolean
```

Sets the translation value for the display list on the Z axis.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View.html#setTranslationZ(kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getTranslationZ()`

### setUseCompositingLayer

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setUseCompositingLayer(
    forceToLayer: Boolean, 
    paint: Paint?
): Boolean
```

Controls whether or not to force this RenderNode to render to an intermediate buffer. Internally RenderNode will already promote itself to a composition layer if it's useful for performance or required for the current combination of `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setAlpha(kotlin.Float)` and `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setHasOverlappingRendering(kotlin.Boolean)`.

The usage of this is instead to allow for either overriding of the internal behavior if it's measured to be necessary for the particular rendering content in question or, more usefully, to add a composition effect to the RenderNode via the optional paint parameter.

Note: When a RenderNode is using a compositing layer it will also result in clipToBounds=true behavior.

| Parameters ||
|---|---|
| `forceToLayer` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if true this forces the RenderNode to use an intermediate buffer. Default \& generally recommended value is false. |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?: The blend mode, alpha, and ColorFilter to apply to the compositing layer. Only applies if forceToLayer is true. The paint's alpha is multiplied with `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#getAlpha()` to resolve the final alpha of the RenderNode. If null then no additional composition effects are applied on top of the composition layer. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the value changed, false if the new value was the same as the previous value. |
