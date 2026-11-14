# EdgeEffect

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EdgeEffect

Kotlin| [Java](../android/widget/EdgeEffect.md) 
| --- | --- |

```
open class EdgeEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.widget.EdgeEffect](../android/widget/EdgeEffect.md) |

This class performs the graphical effect used at the edges of scrollable widgets when the user scrolls beyond the content bounds in 2D space.

EdgeEffect is stateful. Custom widgets using EdgeEffect should create an instance for each edge that should show the effect, feed it input data using the methods [onAbsorb(int)](../android/widget/EdgeEffect.md)), [onPull(float)](../android/widget/EdgeEffect.md)), and [onRelease()](../android/widget/EdgeEffect.md)), and draw the effect using [draw(android.graphics.Canvas)](../android/widget/EdgeEffect.md))in the widget's overridden [android.view.View#draw(Canvas)](../android/view/View.md))method. If [isFinished()](../android/widget/EdgeEffect.md))returns false after drawing, the edge effect's animation is not yet complete and the widget should schedule another drawing pass to continue the animation.

When drawing, widgets should draw their main content and child views first, usually by invoking`super.draw(canvas)`from an overridden`draw`method. (This will invoke onDraw and dispatch drawing to child views as needed.) The edge effect may then be drawn on top of the view's content using the [draw(android.graphics.Canvas)](../android/widget/EdgeEffect.md))method.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EdgeEffect](../android/widget/EdgeEffect.md))`(`context:` ` [Context](../android/content/Context.md)!`)` Construct a new EdgeEffect with a theme appropriate for the provided context. |
| [EdgeEffect](../android/widget/EdgeEffect.md))`(`context:` ` [Context](../android/content/Context.md)`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)?`)` Construct a new EdgeEffect with a theme appropriate for the provided context. |

| Public methods ||
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [draw](../android/widget/EdgeEffect.md))`(`canvas:` ` [Canvas](../android/graphics/Canvas.md)!`)` Draw into the provided canvas. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finish](../android/widget/EdgeEffect.md))`()` Immediately finish the current animation. |
| open [BlendMode](../android/graphics/BlendMode.md)? | [getBlendMode](../android/widget/EdgeEffect.md))`()` Returns the blend mode. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColor](../android/widget/EdgeEffect.md))`()` Return the color of this edge effect in argb. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getDistance](../android/widget/EdgeEffect.md))`()` Returns the pull distance needed to be released to remove the showing effect. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxHeight](../android/widget/EdgeEffect.md))`()` Return the maximum height that the edge effect will be drawn at given the original [input size](../android/widget/EdgeEffect.md)). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFinished](../android/widget/EdgeEffect.md))`()` Reports if this EdgeEffect's animation is finished. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAbsorb](../android/widget/EdgeEffect.md))`(`velocity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Call when the effect absorbs an impact at the given velocity. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPull](../android/widget/EdgeEffect.md))`(`deltaDistance:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` A view should call this when content is pulled away from an edge by the user. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPull](../android/widget/EdgeEffect.md))`(`deltaDistance:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `displacement:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` A view should call this when content is pulled away from an edge by the user. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [onPullDistance](../android/widget/EdgeEffect.md))`(`deltaDistance:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `displacement:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` A view should call this when content is pulled away from an edge by the user. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRelease](../android/widget/EdgeEffect.md))`()` Call when the object is released after being pulled. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBlendMode](../android/widget/EdgeEffect.md))`(`blendmode:` ` [BlendMode](../android/graphics/BlendMode.md)?`)` Set or clear the blend mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColor](../android/widget/EdgeEffect.md))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the color of this edge effect in argb. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSize](../android/widget/EdgeEffect.md))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the size of this edge effect in pixels. |
| --- | --- |

| Properties ||
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [BlendMode](../android/graphics/BlendMode.md)! | [DEFAULT_BLEND_MODE](../android/widget/EdgeEffect.md) The default blend mode used by [EdgeEffect](../android/widget/EdgeEffect.md). |

## Public constructors

### EdgeEffect

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EdgeEffect(context: Context!)
```

Construct a new EdgeEffect with a theme appropriate for the provided context.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:Context used to provide theming and resource information for the EdgeEffect |

### EdgeEffect

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EdgeEffect(
    context: Context, 
    attrs: AttributeSet?)
```

Construct a new EdgeEffect with a theme appropriate for the provided context.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):Context used to provide theming and resource information for the EdgeEffect This value cannot be`null`. |
| `attrs` | [AttributeSet](../android/util/AttributeSet.md)?:The attributes of the XML tag that is inflating the view This value may be`null`. |

## Public methods

### draw

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun draw(canvas: Canvas!): Boolean
```

Draw into the provided canvas. Assumes that the canvas has been rotated accordingly and the size has been set. The effect will be drawn the full width of X=0 to X=width, beginning from Y=0 and extending to some factor \< 1.f of height. The effect will only be visible on a hardware canvas, e.g. [RenderNode.beginRecording()](../android/graphics/RenderNode.md)).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](../android/graphics/Canvas.md)!:Canvas to draw into |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if drawing should continue beyond this frame to continue the animation |

### finish

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun finish(): Unit
```

Immediately finish the current animation. After this call [isFinished()](../android/widget/EdgeEffect.md))will return true. 

### getBlendMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBlendMode(): BlendMode?
```

Returns the blend mode. A blend mode defines how source pixels (generated by a drawing command) are composited with the destination pixels (content of the render target).

<br />

| Return ||
|-----------------------------------------------------------------------------------------------|------------------------------------|
| [BlendMode](../android/graphics/BlendMode.md)? | BlendMode This value may be`null`. |

### getColor

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColor(): Int
```

Return the color of this edge effect in argb.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The color of this edge effect in argb |

### getDistance

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDistance(): Float
```

Returns the pull distance needed to be released to remove the showing effect. It is determined by the [onPull(float,float)](../android/widget/EdgeEffect.md))`deltaDistance`and any animating values, including from [onAbsorb(int)](../android/widget/EdgeEffect.md))and [onRelease()](../android/widget/EdgeEffect.md)). This can be used in conjunction with [onPullDistance(float,float)](../android/widget/EdgeEffect.md))to release the currently showing effect.

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The pull distance that must be released to remove the showing effect. |

### getMaxHeight

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMaxHeight(): Int
```

Return the maximum height that the edge effect will be drawn at given the original [input size](../android/widget/EdgeEffect.md)).

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The maximum height of the edge effect |

### isFinished

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isFinished(): Boolean
```

Reports if this EdgeEffect's animation is finished. If this method returns false after a call to [draw(android.graphics.Canvas)](../android/widget/EdgeEffect.md))the host widget should schedule another drawing pass to continue the animation.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if animation is finished, false if drawing should continue on the next frame. |

### onAbsorb

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAbsorb(velocity: Int): Unit
```

Call when the effect absorbs an impact at the given velocity. Used when a fling reaches the scroll boundary.

When using a [android.widget.Scroller](../android/widget/Scroller.md) or [android.widget.OverScroller](../android/widget/OverScroller.md), the method`getCurrVelocity`will provide a reasonable approximation to use here.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------|
| `velocity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Velocity at impact in pixels per second. |

### onPull

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPull(deltaDistance: Float): Unit
```

A view should call this when content is pulled away from an edge by the user. This will update the state of the current visual effect and its associated animation. The host view should always [android.view.View#invalidate()](../android/view/View.md))after this and draw the results accordingly.

Views using EdgeEffect should favor [onPull(float,float)](../android/widget/EdgeEffect.md))when the displacement of the pull point is known.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `deltaDistance` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Change in distance since the last call. Values may be 0 (no change) to 1.f (full length of the view) or negative values to express change back toward the edge reached to initiate the effect. |

### onPull

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPull(
    deltaDistance: Float, 
    displacement: Float
): Unit
```

A view should call this when content is pulled away from an edge by the user. This will update the state of the current visual effect and its associated animation. The host view should always [android.view.View#invalidate()](../android/view/View.md))after this and draw the results accordingly.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `deltaDistance` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Change in distance since the last call. Values may be 0 (no change) to 1.f (full length of the view) or negative values to express change back toward the edge reached to initiate the effect. |
| `displacement` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The displacement from the starting side of the effect of the point initiating the pull. In the case of touch this is the finger position. Values may be from 0-1. |

### onPullDistance

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPullDistance(
    deltaDistance: Float, 
    displacement: Float
): Float
```

A view should call this when content is pulled away from an edge by the user. This will update the state of the current visual effect and its associated animation. The host view should always [android.view.View#invalidate()](../android/view/View.md))after this and draw the results accordingly. This works similarly to [onPull(float,float)](../android/widget/EdgeEffect.md)), but returns the amount of`deltaDistance`that has been consumed. If the [getDistance()](../android/widget/EdgeEffect.md))is currently 0 and`deltaDistance`is negative, this function will return 0 and the drawn value will remain unchanged. This method can be used to reverse the effect from a pull or absorb and partially consume some of a motion: 

```kotlin
if (deltaY < 0) {
          float consumed = edgeEffect.onPullDistance(deltaY / getHeight(), x / getWidth());
          deltaY -= consumed * getHeight();
          if (edgeEffect.getDistance() == 0f) edgeEffect.onRelease();
      }
  
```

<br />

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `deltaDistance` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Change in distance since the last call. Values may be 0 (no change) to 1.f (full length of the view) or negative values to express change back toward the edge reached to initiate the effect. |
| `displacement` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The displacement from the starting side of the effect of the point initiating the pull. In the case of touch this is the finger position. Values may be from 0-1. |

| Return ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The amount of`deltaDistance`that was consumed, a number between 0 and`deltaDistance`. |

### onRelease

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onRelease(): Unit
```

Call when the object is released after being pulled. This will begin the "decay" phase of the effect. After calling this method the host view should [android.view.View#invalidate()](../android/view/View.md))and thereby draw the results accordingly. 

### setBlendMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setBlendMode(blendmode: BlendMode?): Unit
```

Set or clear the blend mode. A blend mode defines how source pixels (generated by a drawing command) are composited with the destination pixels (content of the render target).

<br />

Pass null to clear any previous blend mode.

<br />

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `blendmode` | [BlendMode](../android/graphics/BlendMode.md)?:May be null. The blend mode to be installed in the paint |

**See Also**

- [android.graphics.BlendMode](../android/graphics/BlendMode.md) 

### setColor

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setColor(color: Int): Unit
```

Set the color of this edge effect in argb.

| Parameters ||
|---------|------------------------------------------------------------------------------------------|
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Color in argb |

### setSize

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSize(
    width: Int, 
    height: Int
): Unit
```

Set the size of this edge effect in pixels.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Effect width in pixels |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Effect height in pixels |

## Properties

### DEFAULT_BLEND_MODE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFAULT_BLEND_MODE: BlendMode!
```

The default blend mode used by [EdgeEffect](../android/widget/EdgeEffect.md).
