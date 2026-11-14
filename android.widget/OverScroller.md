# OverScroller

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OverScroller

Kotlin | [Java](OverScroller.md) 
| --- | --- |

```
open class OverScroller
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.widget.OverScroller](OverScroller.md) |

This class encapsulates scrolling with the ability to overshoot the bounds of a scrolling operation. This class is a drop-in replacement for [android.widget.Scroller](Scroller.md) in most cases.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [OverScroller](OverScroller.md))`(`context:` ` [Context](../android.content/Context.md)!`)` Creates an OverScroller with a viscous fluid scroll interpolator and flywheel. |
| [OverScroller](OverScroller.md))`(`context:` ` [Context](../android.content/Context.md)!`, `interpolator:` ` [Interpolator](../android.view.animation/Interpolator.md)!`)` Creates an OverScroller with flywheel enabled. |
| [OverScroller](OverScroller.md))`(`context:` ` [Context](../android.content/Context.md)!`, `interpolator:` ` [Interpolator](../android.view.animation/Interpolator.md)!`, `bounceCoefficientX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bounceCoefficientY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Creates an OverScroller with flywheel enabled. |
| [OverScroller](OverScroller.md))`(`context:` ` [Context](../android.content/Context.md)!`, `interpolator:` ` [Interpolator](../android.view.animation/Interpolator.md)!`, `bounceCoefficientX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bounceCoefficientY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `flywheel:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates an OverScroller. |

| Public methods ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [abortAnimation](OverScroller.md))`()` Stops the animation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [computeScrollOffset](OverScroller.md))`()` Call this when you want to know the new location. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fling](OverScroller.md))`(`startX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `velocityX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `velocityY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fling](OverScroller.md))`(`startX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `velocityX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `velocityY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `overX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `overY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Start scrolling based on a fling gesture. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forceFinished](OverScroller.md))`(`finished:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Force the finished field to a particular value. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getCurrVelocity](OverScroller.md))`()` Returns the absolute value of the current velocity. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCurrX](OverScroller.md))`()` Returns the current X offset in the scroll. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCurrY](OverScroller.md))`()` Returns the current Y offset in the scroll. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFinalX](OverScroller.md))`()` Returns where the scroll will end. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFinalY](OverScroller.md))`()` Returns where the scroll will end. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStartX](OverScroller.md))`()` Returns the start X offset in the scroll. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStartY](OverScroller.md))`()` Returns the start Y offset in the scroll. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFinished](OverScroller.md))`()` Returns whether the scroller has finished scrolling. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOverScrolled](OverScroller.md))`()` Returns whether the current Scroller is currently returning to a valid position. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyHorizontalEdgeReached](OverScroller.md))`(`startX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `finalX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `overX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Notify the scroller that we've reached a horizontal boundary. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyVerticalEdgeReached](OverScroller.md))`(`startY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `finalY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `overY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Notify the scroller that we've reached a vertical boundary. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFriction](OverScroller.md))`(`friction:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` The amount of friction applied to flings. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [springBack](OverScroller.md))`(`startX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Call this when you want to 'spring back' into a valid coordinate range. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startScroll](OverScroller.md))`(`startX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dx:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Start scrolling by providing a starting point and the distance to travel. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startScroll](OverScroller.md))`(`startX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dx:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `duration:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Start scrolling by providing a starting point and the distance to travel. |

## Public constructors

### OverScroller

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OverScroller(context: Context!)
```

Creates an OverScroller with a viscous fluid scroll interpolator and flywheel.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!: |

### OverScroller

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OverScroller(
    context: Context!, 
    interpolator: Interpolator!)
```

Creates an OverScroller with flywheel enabled.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!: The context of this application. |
| `interpolator` | [Interpolator](../android.view.animation/Interpolator.md)!: The scroll interpolator. If null, a default (viscous) interpolator will be used. |

### OverScroller

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OverScroller(
    context: Context!, 
    interpolator: Interpolator!, 
    bounceCoefficientX: Float, 
    bounceCoefficientY: Float)
```

**Deprecated:** *Use [OverScroller(android.content.Context,android.view.animation.Interpolator)](OverScroller.md)) instead.*

Creates an OverScroller with flywheel enabled.

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!: The context of this application. |
| `interpolator` | [Interpolator](../android.view.animation/Interpolator.md)!: The scroll interpolator. If null, a default (viscous) interpolator will be used. |
| `bounceCoefficientX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): A value between 0 and 1 that will determine the proportion of the velocity which is preserved in the bounce when the horizontal edge is reached. A null value means no bounce. This behavior is no longer supported and this coefficient has no effect. |
| --- | --- |
| `bounceCoefficientY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Same as bounceCoefficientX but for the vertical direction. This behavior is no longer supported and this coefficient has no effect. |

### OverScroller

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OverScroller(
    context: Context!, 
    interpolator: Interpolator!, 
    bounceCoefficientX: Float, 
    bounceCoefficientY: Float, 
    flywheel: Boolean)
```

**Deprecated:** *Use [OverScroller(android.content.Context,android.view.animation.Interpolator)](OverScroller.md)) instead.*

Creates an OverScroller.

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!: The context of this application. |
| `interpolator` | [Interpolator](../android.view.animation/Interpolator.md)!: The scroll interpolator. If null, a default (viscous) interpolator will be used. |
| `bounceCoefficientX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): A value between 0 and 1 that will determine the proportion of the velocity which is preserved in the bounce when the horizontal edge is reached. A null value means no bounce. This behavior is no longer supported and this coefficient has no effect. |
| --- | --- |
| `bounceCoefficientY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Same as bounceCoefficientX but for the vertical direction. This behavior is no longer supported and this coefficient has no effect. |
| `flywheel` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, successive fling motions will keep on increasing scroll speed. |

## Public methods

### abortAnimation

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun abortAnimation(): Unit
```

Stops the animation. Contrary to [forceFinished(boolean)](OverScroller.md)), aborting the animating causes the scroller to move to the final x and y positions. 
**See Also**

- [#forceFinished(boolean)](OverScroller.md)) 

### computeScrollOffset

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun computeScrollOffset(): Boolean
```

Call this when you want to know the new location. If it returns true, the animation is not yet finished. 

### fling

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun fling(
    startX: Int, 
    startY: Int, 
    velocityX: Int, 
    velocityY: Int, 
    minX: Int, 
    maxX: Int, 
    minY: Int, 
    maxY: Int
): Unit
```  

### fling

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun fling(
    startX: Int, 
    startY: Int, 
    velocityX: Int, 
    velocityY: Int, 
    minX: Int, 
    maxX: Int, 
    minY: Int, 
    maxY: Int, 
    overX: Int, 
    overY: Int
): Unit
```

Start scrolling based on a fling gesture. The distance traveled will depend on the initial velocity of the fling.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `startX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Starting point of the scroll (X) |
| `startY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Starting point of the scroll (Y) |
| `velocityX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Initial velocity of the fling (X) measured in pixels per second. |
| --- | --- |
| `velocityY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Initial velocity of the fling (Y) measured in pixels per second |
| `minX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Minimum X value. The scroller will not scroll past this point unless overX \> 0. If overfling is allowed, it will use minX as a springback boundary. |
| `maxX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Maximum X value. The scroller will not scroll past this point unless overX \> 0. If overfling is allowed, it will use maxX as a springback boundary. |
| --- | --- |
| `minY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Minimum Y value. The scroller will not scroll past this point unless overY \> 0. If overfling is allowed, it will use minY as a springback boundary. |
| `maxY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Maximum Y value. The scroller will not scroll past this point unless overY \> 0. If overfling is allowed, it will use maxY as a springback boundary. |
| `overX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Overfling range. If \> 0, horizontal overfling in either direction will be possible. |
| --- | --- |
| `overY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Overfling range. If \> 0, vertical overfling in either direction will be possible. |

### forceFinished

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun forceFinished(finished: Boolean): Unit
```

Force the finished field to a particular value. Contrary to [abortAnimation()](OverScroller.md)), forcing the animation to finished does NOT cause the scroller to move to the final x and y position.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `finished` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The new finished value. |

### getCurrVelocity

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurrVelocity(): Float
```

Returns the absolute value of the current velocity.

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The original velocity less the deceleration, norm of the X and Y velocity vector. |

### getCurrX

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCurrX(): Int
```

Returns the current X offset in the scroll.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The new X offset as an absolute distance from the origin. |

### getCurrY

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCurrY(): Int
```

Returns the current Y offset in the scroll.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The new Y offset as an absolute distance from the origin. |

### getFinalX

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFinalX(): Int
```

Returns where the scroll will end. Valid only for "fling" scrolls.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The final X offset as an absolute distance from the origin. |

### getFinalY

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFinalY(): Int
```

Returns where the scroll will end. Valid only for "fling" scrolls.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The final Y offset as an absolute distance from the origin. |

### getStartX

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStartX(): Int
```

Returns the start X offset in the scroll.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The start X offset as an absolute distance from the origin. |

### getStartY

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStartY(): Int
```

Returns the start Y offset in the scroll.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The start Y offset as an absolute distance from the origin. |

### isFinished

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isFinished(): Boolean
```

Returns whether the scroller has finished scrolling.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the scroller has finished scrolling, false otherwise. |

### isOverScrolled

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isOverScrolled(): Boolean
```

Returns whether the current Scroller is currently returning to a valid position. Valid bounds were provided by the [fling(int,int,int,int,int,int,int,int,int,int)](OverScroller.md)) method. One should check this value before calling [startScroll(int,int,int,int)](OverScroller.md)) as the interpolation currently in progress to restore a valid position will then be stopped. The caller has to take into account the fact that the started scroll will start from an overscrolled position.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true when the current position is overscrolled and in the process of interpolating back to a valid value. |

### notifyHorizontalEdgeReached

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun notifyHorizontalEdgeReached(
    startX: Int, 
    finalX: Int, 
    overX: Int
): Unit
```

Notify the scroller that we've reached a horizontal boundary. Normally the information to handle this will already be known when the animation is started, such as in a call to one of the fling functions. However there are cases where this cannot be known in advance. This function will transition the current motion and animate from startX to finalX as appropriate.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `startX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Starting/current X position |
| `finalX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Desired final X position |
| `overX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Magnitude of overscroll allowed. This should be the maximum desired distance from finalX. Absolute value - must be positive. |
| --- | --- |

### notifyVerticalEdgeReached

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun notifyVerticalEdgeReached(
    startY: Int, 
    finalY: Int, 
    overY: Int
): Unit
```

Notify the scroller that we've reached a vertical boundary. Normally the information to handle this will already be known when the animation is started, such as in a call to one of the fling functions. However there are cases where this cannot be known in advance. This function will animate a parabolic motion from startY to finalY.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `startY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Starting/current Y position |
| `finalY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Desired final Y position |
| `overY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Magnitude of overscroll allowed. This should be the maximum desired distance from finalY. Absolute value - must be positive. |
| --- | --- |

### setFriction

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setFriction(friction: Float): Unit
```

The amount of friction applied to flings. The default value is [ViewConfiguration.getScrollFriction](../android.view/ViewConfiguration.md)).

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `friction` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): A scalar dimension-less value representing the coefficient of friction. |

### springBack

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun springBack(
    startX: Int, 
    startY: Int, 
    minX: Int, 
    maxX: Int, 
    minY: Int, 
    maxY: Int
): Boolean
```

Call this when you want to 'spring back' into a valid coordinate range.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------|
| `startX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Starting X coordinate |
| `startY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Starting Y coordinate |
| `minX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Minimum valid X value |
| --- | --- |
| `maxX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Maximum valid X value |
| `minY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Minimum valid Y value |
| `maxY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Minimum valid Y value |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if a springback was initiated, false if startX and startY were already within the valid range. |

### startScroll

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startScroll(
    startX: Int, 
    startY: Int, 
    dx: Int, 
    dy: Int
): Unit
```

Start scrolling by providing a starting point and the distance to travel. The scroll will use the default value of 250 milliseconds for the duration.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `startX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Starting horizontal scroll offset in pixels. Positive numbers will scroll the content to the left. |
| `startY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Starting vertical scroll offset in pixels. Positive numbers will scroll the content up. |
| `dx` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Horizontal distance to travel. Positive numbers will scroll the content to the left. |
| --- | --- |
| `dy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Vertical distance to travel. Positive numbers will scroll the content up. |

### startScroll

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startScroll(
    startX: Int, 
    startY: Int, 
    dx: Int, 
    dy: Int, 
    duration: Int
): Unit
```

Start scrolling by providing a starting point and the distance to travel.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `startX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Starting horizontal scroll offset in pixels. Positive numbers will scroll the content to the left. |
| `startY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Starting vertical scroll offset in pixels. Positive numbers will scroll the content up. |
| `dx` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Horizontal distance to travel. Positive numbers will scroll the content to the left. |
| --- | --- |
| `dy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Vertical distance to travel. Positive numbers will scroll the content up. |
| `duration` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Duration of the scroll in milliseconds. |
