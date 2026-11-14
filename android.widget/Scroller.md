# Scroller

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Scroller

Kotlin| [Java](Scroller.md) 
| --- | --- |

```
open class Scroller
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.widget.Scroller](Scroller.md) |

This class encapsulates scrolling. You can use scrollers ([Scroller](Scroller.md) or [OverScroller](OverScroller.md)) to collect the data you need to produce a scrolling animation---for example, in response to a fling gesture. Scrollers track scroll offsets for you over time, but they don't automatically apply those positions to your view. It's your responsibility to get and apply new coordinates at a rate that will make the scrolling animation look smooth.

Here is a simple example: 

```kotlin
private Scroller mScroller = new Scroller(context);
  ...
  public void zoomIn() {
      // Revert any animation currently in progress
      mScroller.forceFinished(true);
      // Start scrolling by providing a starting point and
      // the distance to travel
      mScroller.startScroll(0, 0, 100, 0);
      // Invalidate to request a redraw
      invalidate();
  }
```

To track the changing positions of the x/y coordinates, use [computeScrollOffset](Scroller.md)). The method returns a boolean to indicate whether the scroller is finished. If it isn't, it means that a fling or programmatic pan operation is still in progress. You can use this method to find the current offsets of the x and y coordinates, for example: 

```kotlin
if (mScroller.computeScrollOffset()) {
      // Get current x and y positions
      int currX = mScroller.getCurrX();
      int currY = mScroller.getCurrY();
     ...
  }
```

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Scroller](Scroller.md))`(`context:` ` [Context](../android.content/Context.md)!`)` Create a Scroller with the default duration and interpolator. |
| [Scroller](Scroller.md))`(`context:` ` [Context](../android.content/Context.md)!`, `interpolator:` ` [Interpolator](../android.view.animation/Interpolator.md)!`)` Create a Scroller with the specified interpolator. |
| [Scroller](Scroller.md))`(`context:` ` [Context](../android.content/Context.md)!`, `interpolator:` ` [Interpolator](../android.view.animation/Interpolator.md)!`, `flywheel:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Create a Scroller with the specified interpolator. |

| Public methods ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [abortAnimation](Scroller.md))`()` Stops the animation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [computeScrollOffset](Scroller.md))`()` Call this when you want to know the new location. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [extendDuration](Scroller.md))`(`extend:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Extend the scroll animation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fling](Scroller.md))`(`startX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `velocityX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `velocityY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Start scrolling based on a fling gesture. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forceFinished](Scroller.md))`(`finished:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Force the finished field to a particular value. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getCurrVelocity](Scroller.md))`()` Returns the current velocity. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCurrX](Scroller.md))`()` Returns the current X offset in the scroll. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCurrY](Scroller.md))`()` Returns the current Y offset in the scroll. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDuration](Scroller.md))`()` Returns how long the scroll event will take, in milliseconds. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFinalX](Scroller.md))`()` Returns where the scroll will end. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFinalY](Scroller.md))`()` Returns where the scroll will end. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStartX](Scroller.md))`()` Returns the start X offset in the scroll. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStartY](Scroller.md))`()` Returns the start Y offset in the scroll. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFinished](Scroller.md))`()` Returns whether the scroller has finished scrolling. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFinalX](Scroller.md))`(`newX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the final position (X) for this scroller. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFinalY](Scroller.md))`(`newY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the final position (Y) for this scroller. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFriction](Scroller.md))`(`friction:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` The amount of friction applied to flings. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startScroll](Scroller.md))`(`startX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dx:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Start scrolling by providing a starting point and the distance to travel. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startScroll](Scroller.md))`(`startX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dx:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `duration:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Start scrolling by providing a starting point, the distance to travel, and the duration of the scroll. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [timePassed](Scroller.md))`()` Returns the time elapsed since the beginning of the scrolling. |

## Public constructors

### Scroller

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Scroller(context: Context!)
```

Create a Scroller with the default duration and interpolator. 

### Scroller

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Scroller(
    context: Context!, 
    interpolator: Interpolator!)
```

Create a Scroller with the specified interpolator. If the interpolator is null, the default (viscous) interpolator will be used. "Flywheel" behavior will be in effect for apps targeting Honeycomb or newer. 

### Scroller

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Scroller(
    context: Context!, 
    interpolator: Interpolator!, 
    flywheel: Boolean)
```

Create a Scroller with the specified interpolator. If the interpolator is null, the default (viscous) interpolator will be used. Specify whether or not to support progressive "flywheel" behavior in flinging.

## Public methods

### abortAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun abortAnimation(): Unit
```

Stops the animation. Contrary to [forceFinished(boolean)](Scroller.md)), aborting the animating cause the scroller to move to the final x and y position 
**See Also**

- [#forceFinished(boolean)](Scroller.md)) 

### computeScrollOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun computeScrollOffset(): Boolean
```

Call this when you want to know the new location. If it returns true, the animation is not yet finished. 

### extendDuration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun extendDuration(extend: Int): Unit
```

Extend the scroll animation. This allows a running animation to scroll further and longer, when used with [setFinalX(int)](Scroller.md))or [setFinalY(int)](Scroller.md)).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------|
| `extend` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional time to scroll in milliseconds. |

**See Also**

- [#setFinalX(int)](Scroller.md))
- [#setFinalY(int)](Scroller.md)) 

### fling

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Start scrolling based on a fling gesture. The distance travelled will depend on the initial velocity of the fling.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `startX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Starting point of the scroll (X) |
| `startY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Starting point of the scroll (Y) |
| `velocityX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Initial velocity of the fling (X) measured in pixels per second. |
| --- | --- |
| `velocityY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Initial velocity of the fling (Y) measured in pixels per second |
| `minX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Minimum X value. The scroller will not scroll past this point. |
| `maxX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Maximum X value. The scroller will not scroll past this point. |
| --- | --- |
| `minY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Minimum Y value. The scroller will not scroll past this point. |
| `maxY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Maximum Y value. The scroller will not scroll past this point. |

### forceFinished

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun forceFinished(finished: Boolean): Unit
```

Force the finished field to a particular value.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------|
| `finished` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):The new finished value. |

### getCurrVelocity

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurrVelocity(): Float
```

Returns the current velocity.

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The original velocity less the deceleration. Result may be negative. |

### getCurrX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCurrX(): Int
```

Returns the current X offset in the scroll.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The new X offset as an absolute distance from the origin. |

### getCurrY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCurrY(): Int
```

Returns the current Y offset in the scroll.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The new Y offset as an absolute distance from the origin. |

### getDuration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDuration(): Int
```

Returns how long the scroll event will take, in milliseconds.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The duration of the scroll in milliseconds. |

### getFinalX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFinalX(): Int
```

Returns where the scroll will end. Valid only for "fling" scrolls.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The final X offset as an absolute distance from the origin. |

### getFinalY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFinalY(): Int
```

Returns where the scroll will end. Valid only for "fling" scrolls.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The final Y offset as an absolute distance from the origin. |

### getStartX

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStartX(): Int
```

Returns the start X offset in the scroll.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The start X offset as an absolute distance from the origin. |

### getStartY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStartY(): Int
```

Returns the start Y offset in the scroll.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The start Y offset as an absolute distance from the origin. |

### isFinished

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isFinished(): Boolean
```

Returns whether the scroller has finished scrolling.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the scroller has finished scrolling, false otherwise. |

### setFinalX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFinalX(newX: Int): Unit
```

Sets the final position (X) for this scroller.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------|
| `newX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new X offset as an absolute distance from the origin. |

**See Also**

- [#extendDuration(int)](Scroller.md))
- [#setFinalY(int)](Scroller.md)) 

### setFinalY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFinalY(newY: Int): Unit
```

Sets the final position (Y) for this scroller.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------|
| `newY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new Y offset as an absolute distance from the origin. |

**See Also**

- [#extendDuration(int)](Scroller.md))
- [#setFinalX(int)](Scroller.md)) 

### setFriction

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setFriction(friction: Float): Unit
```

The amount of friction applied to flings. The default value is [ViewConfiguration.getScrollFriction](../android.view/ViewConfiguration.md)).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `friction` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):A scalar dimension-less value representing the coefficient of friction. |

### startScroll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `startX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Starting horizontal scroll offset in pixels. Positive numbers will scroll the content to the left. |
| `startY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Starting vertical scroll offset in pixels. Positive numbers will scroll the content up. |
| `dx` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Horizontal distance to travel. Positive numbers will scroll the content to the left. |
| --- | --- |
| `dy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Vertical distance to travel. Positive numbers will scroll the content up. |

### startScroll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startScroll(
    startX: Int, 
    startY: Int, 
    dx: Int, 
    dy: Int, 
    duration: Int
): Unit
```

Start scrolling by providing a starting point, the distance to travel, and the duration of the scroll.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `startX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Starting horizontal scroll offset in pixels. Positive numbers will scroll the content to the left. |
| `startY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Starting vertical scroll offset in pixels. Positive numbers will scroll the content up. |
| `dx` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Horizontal distance to travel. Positive numbers will scroll the content to the left. |
| --- | --- |
| `dy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Vertical distance to travel. Positive numbers will scroll the content up. |
| `duration` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Duration of the scroll in milliseconds. |

### timePassed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun timePassed(): Int
```

Returns the time elapsed since the beginning of the scrolling.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The elapsed time in milliseconds. |
