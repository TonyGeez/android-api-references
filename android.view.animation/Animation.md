Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Animation

Kotlin | [Java](https://developer.android.com/reference/android/view/animation/Animation "View this page in Java")

```
abstract class Animation : Cloneable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.animation.Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation#) |

| Known Direct Subclasses [AlphaAnimation](https://developer.android.com/reference/kotlin/android/view/animation/AlphaAnimation), [AnimationSet](https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet), [RotateAnimation](https://developer.android.com/reference/kotlin/android/view/animation/RotateAnimation), [ScaleAnimation](https://developer.android.com/reference/kotlin/android/view/animation/ScaleAnimation), [TranslateAnimation](https://developer.android.com/reference/kotlin/android/view/animation/TranslateAnimation) |---|---| | [AlphaAnimation](https://developer.android.com/reference/kotlin/android/view/animation/AlphaAnimation) | An animation that controls the alpha level of an object. | | [AnimationSet](https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet) | Represents a group of Animations that should be played together. | | [RotateAnimation](https://developer.android.com/reference/kotlin/android/view/animation/RotateAnimation) | An animation that controls the rotation of an object. | | [ScaleAnimation](https://developer.android.com/reference/kotlin/android/view/animation/ScaleAnimation) | An animation that controls the scale of an object. | | [TranslateAnimation](https://developer.android.com/reference/kotlin/android/view/animation/TranslateAnimation) | An animation that controls the position of an object. | |

Abstraction for an Animation that can be applied to Views, Surfaces, or other objects. See the `https://developer.android.com/reference/kotlin/android/view/animation/package-summary`.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/view/animation/Animation.AnimationListener` An animation listener receives notifications from an animation. |
| open | `https://developer.android.com/reference/kotlin/android/view/animation/Animation.Description` Utility class to parse a string description of a size. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#ABSOLUTE:kotlin.Int` The specified dimension is an absolute number of pixels. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#INFINITE:kotlin.Int` Repeat the animation indefinitely. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#RELATIVE_TO_PARENT:kotlin.Int` The specified dimension holds a float and should be multiplied by the height or width of the parent of the object being animated. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#RELATIVE_TO_SELF:kotlin.Int` The specified dimension holds a float and should be multiplied by the height or width of the object being animated. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#RESTART:kotlin.Int` When the animation reaches the end and the repeat count is INFINTE_REPEAT or a positive value, the animation restarts from the beginning. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#REVERSE:kotlin.Int` When the animation reaches the end and the repeat count is INFINTE_REPEAT or a positive value, the animation plays backward (and then forward again). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#START_ON_FIRST_FRAME:kotlin.Int` Can be used as the start time to indicate the start time should be the current time when `https://developer.android.com/reference/kotlin/android/view/animation/Animation#getTransformation(kotlin.Long,%20android.view.animation.Transformation)` is invoked for the first animation frame. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#ZORDER_BOTTOM:kotlin.Int` Requests that the content being animated be forced under all other content for the duration of the animation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#ZORDER_NORMAL:kotlin.Int` Requests that the content being animated be kept in its current Z order. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#ZORDER_TOP:kotlin.Int` Requests that the content being animated be forced on top of all other content for the duration of the animation. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/animation/Animation#Animation()()` Creates a new animation with a duration of 0ms, the default interpolator, with fillBefore set to true and fillAfter set to false |
| `https://developer.android.com/reference/kotlin/android/view/animation/Animation#Animation(android.content.Context,%20android.util.AttributeSet)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#!)` Creates a new animation whose parameters come from the specified context and attributes set. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#cancel()()` Cancel the animation. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#computeDurationHint()()` Compute a hint at how long the entire animation may last, in milliseconds. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#getBackdropColor()()` Returns the background color to show behind the animating windows. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#getBackgroundColor()()` Returns the background color behind the animation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#getDetachWallpaper()()` Return value of `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setDetachWallpaper(kotlin.Boolean)`. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#getDuration()()` How long this animation should last |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#getFillAfter()()` If fillAfter is true, this animation will apply its transformation after the end time of the animation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#getFillBefore()()` If fillBefore is true, this animation will apply its transformation before the start time of the animation. |
| open [Interpolator](https://developer.android.com/reference/kotlin/android/view/animation/Interpolator)! | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#getInterpolator()()` Gets the acceleration curve type for this animation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#getRepeatCount()()` Defines how many times the animation should repeat. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#getRepeatMode()()` Defines what this animation should do when it reaches the end. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#getShowBackdrop()()` If showBackdrop is `true` and this animation is applied on a window, then the windows in the animation will animate with the background associated with this window behind them. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#getStartOffset()()` When this animation should start, relative to StartTime |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#getStartTime()()` When this animation should start. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#getTransformation(kotlin.Long,%20android.view.animation.Transformation)(currentTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, outTransformation: https://developer.android.com/reference/kotlin/android/view/animation/Transformation!)` Gets the transformation to apply at a specified point in time. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#getTransformation(kotlin.Long,%20android.view.animation.Transformation,%20kotlin.Float)(currentTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, outTransformation: https://developer.android.com/reference/kotlin/android/view/animation/Transformation!, scale: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Gets the transformation to apply at a specified point in time. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#getZAdjustment()()` Returns the Z ordering mode to use while running the animation as previously set by `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setZAdjustment(kotlin.Int)`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#hasEnded()()` Indicates whether this animation has ended or not. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#hasStarted()()` Indicates whether this animation has started or not. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#initialize(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, parentWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, parentHeight: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Initialize this animation with the dimensions of the object being animated as well as the objects parents. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#isFillEnabled()()` If fillEnabled is true, this animation will apply the value of fillBefore. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#isInitialized()()` Whether or not the animation has been initialized. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#reset()()` Reset the initialization state of this animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#restrictDuration(kotlin.Long)(durationMillis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Ensure that the duration that this animation will run is not longer than durationMillis. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#scaleCurrentDuration(kotlin.Float)(scale: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` How much to scale the duration by. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setAnimationListener(android.view.animation.Animation.AnimationListener)(listener: https://developer.android.com/reference/kotlin/android/view/animation/Animation.AnimationListener!)` Binds an animation listener to this animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setBackdropColor(kotlin.Int)(backdropColor: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the color to use for the backdrop shown behind the animating windows. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setBackgroundColor(kotlin.Int)(bg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set background behind animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setDetachWallpaper(kotlin.Boolean)(detachWallpaper: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` If detachWallpaper is true, and this is a window animation of a window that has a wallpaper background, then the window will be detached from the wallpaper while it runs. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setDuration(kotlin.Long)(durationMillis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` How long this animation should last. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setFillAfter(kotlin.Boolean)(fillAfter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` If fillAfter is true, the transformation that this animation performed will persist when it is finished. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setFillBefore(kotlin.Boolean)(fillBefore: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` If fillBefore is true, this animation will apply its transformation before the start time of the animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setFillEnabled(kotlin.Boolean)(fillEnabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` If fillEnabled is true, the animation will apply the value of fillBefore. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setInterpolator(android.content.Context,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, resID: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the acceleration curve for this animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setInterpolator(android.view.animation.Interpolator)(i: https://developer.android.com/reference/kotlin/android/view/animation/Interpolator!)` Sets the acceleration curve for this animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setRepeatCount(kotlin.Int)(repeatCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets how many times the animation should be repeated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setRepeatMode(kotlin.Int)(repeatMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Defines what this animation should do when it reaches the end. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setShowBackdrop(kotlin.Boolean)(showBackdrop: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` If showBackdrop is `true` and this animation is applied on a window, then the windows in the animation will animate with the background associated with this window behind them. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setStartOffset(kotlin.Long)(startOffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` When this animation should start relative to the start time. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setStartTime(kotlin.Long)(startTimeMillis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` When this animation should start. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setZAdjustment(kotlin.Int)(zAdjustment: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the Z ordering mode to use while running the animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#start()()` Convenience method to start the animation the first time `https://developer.android.com/reference/kotlin/android/view/animation/Animation#getTransformation(kotlin.Long,%20android.view.animation.Transformation)` is invoked. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#startNow()()` Convenience method to start the animation at the current time in milliseconds. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#willChangeBounds()()` Indicates whether or not this animation will affect the bounds of the animated view. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#willChangeTransformationMatrix()()` Indicates whether or not this animation will affect the transformation matrix. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#applyTransformation(kotlin.Float,%20android.view.animation.Transformation)(interpolatedTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, t: https://developer.android.com/reference/kotlin/android/view/animation/Transformation!)` Helper for getTransformation. |
| open [Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation#) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#clone()()` Creates and returns a copy of this object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#ensureInterpolator()()` Gurantees that this animation has an interpolator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#finalize()()` Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#getScaleFactor()()` The scale factor is set by the call to `getTransformation`. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#resolveSize(kotlin.Int,%20kotlin.Float,%20kotlin.Int,%20kotlin.Int)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, size: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, parentSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Convert the information in the description of a size to an actual dimension |

## Constants

### ABSOLUTE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ABSOLUTE: Int
```

The specified dimension is an absolute number of pixels.

 Value: 0

### INFINITE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INFINITE: Int
```

Repeat the animation indefinitely.

 Value: -1

### RELATIVE_TO_PARENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RELATIVE_TO_PARENT: Int
```

The specified dimension holds a float and should be multiplied by the height or width of the parent of the object being animated.

 Value: 2

### RELATIVE_TO_SELF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RELATIVE_TO_SELF: Int
```

The specified dimension holds a float and should be multiplied by the height or width of the object being animated.

 Value: 1

### RESTART

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESTART: Int
```

When the animation reaches the end and the repeat count is INFINTE_REPEAT or a positive value, the animation restarts from the beginning.

 Value: 1

### REVERSE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REVERSE: Int
```

When the animation reaches the end and the repeat count is INFINTE_REPEAT or a positive value, the animation plays backward (and then forward again).

 Value: 2

### START_ON_FIRST_FRAME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_ON_FIRST_FRAME: Int
```

Can be used as the start time to indicate the start time should be the current time when `https://developer.android.com/reference/kotlin/android/view/animation/Animation#getTransformation(kotlin.Long,%20android.view.animation.Transformation)` is invoked for the first animation frame. This can is useful for short animations.

 Value: -1

### ZORDER_BOTTOM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ZORDER_BOTTOM: Int
```

Requests that the content being animated be forced under all other content for the duration of the animation.

 Value: -1

### ZORDER_NORMAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ZORDER_NORMAL: Int
```

Requests that the content being animated be kept in its current Z order.

 Value: 0

### ZORDER_TOP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ZORDER_TOP: Int
```

Requests that the content being animated be forced on top of all other content for the duration of the animation.

 Value: 1

## Public constructors

### Animation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Animation()
```

Creates a new animation with a duration of 0ms, the default interpolator, with fillBefore set to true and fillAfter set to false

### Animation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Animation(
    context: Context!, 
    attrs: AttributeSet!)
```

Creates a new animation whose parameters come from the specified context and attributes set.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: the application environment |
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!: the set of attributes holding the animation parameters |

## Public methods

### cancel

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cancel(): Unit
```

Cancel the animation. Cancelling an animation invokes the animation listener, if set, to notify the end of the animation. If you cancel an animation manually, you must call `https://developer.android.com/reference/kotlin/android/view/animation/Animation#reset()` before starting the animation again.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/animation/Animation#reset()`
- `https://developer.android.com/reference/kotlin/android/view/animation/Animation#start()`
- `https://developer.android.com/reference/kotlin/android/view/animation/Animation#startNow()`

### computeDurationHint

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun computeDurationHint(): Long
```

Compute a hint at how long the entire animation may last, in milliseconds. Animations can be written to cause themselves to run for a different duration than what is computed here, but generally this should be accurate.

### getBackdropColor

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBackdropColor(): Int
```

Returns the background color to show behind the animating windows. Will only show the background if showBackdrop was set to true. See `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setShowBackdrop(kotlin.Boolean)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The backdrop color. If 0, the backdrop color will not apply. |

### getBackgroundColor

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBackgroundColor(): Int
```

**Deprecated:** *None of window animations are running with background color.*

Returns the background color behind the animation.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/animation/Animation#getBackdropColor()`

### getDetachWallpaper

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDetachWallpaper(): Boolean
```

**Deprecated:** *All window animations are running with detached wallpaper.*

Return value of `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setDetachWallpaper(kotlin.Boolean)`.

### getDuration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDuration(): Long
```

How long this animation should last

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the duration in milliseconds of the animation |

### getFillAfter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFillAfter(): Boolean
```

If fillAfter is true, this animation will apply its transformation after the end time of the animation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the animation applies its transformation after it ends |

### getFillBefore

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFillBefore(): Boolean
```

If fillBefore is true, this animation will apply its transformation before the start time of the animation. If fillBefore is false and `https://developer.android.com/reference/kotlin/android/view/animation/Animation#isFillEnabled()` is true, the transformation will not be applied until the start time of the animation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the animation applies its transformation before it starts |

### getInterpolator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInterpolator(): Interpolator!
```

Gets the acceleration curve type for this animation.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/animation/Interpolator!` | the `https://developer.android.com/reference/kotlin/android/view/animation/Interpolator` associated to this animation |

### getRepeatCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRepeatCount(): Int
```

Defines how many times the animation should repeat. The default value is 0.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of times the animation should repeat, or `https://developer.android.com/reference/kotlin/android/view/animation/Animation#INFINITE:kotlin.Int` |

### getRepeatMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRepeatMode(): Int
```

Defines what this animation should do when it reaches the end.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | either one of `https://developer.android.com/reference/kotlin/android/view/animation/Animation#REVERSE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/animation/Animation#RESTART:kotlin.Int` |

### getShowBackdrop

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getShowBackdrop(): Boolean
```

If showBackdrop is `true` and this animation is applied on a window, then the windows in the animation will animate with the background associated with this window behind them. If no backdrop color is explicitly set, the backdrop's color comes from the `https://developer.android.com/reference/kotlin/android/R.styleable.html#Theme_colorBackground:kotlin.Int` that is applied to this window through its theme. If multiple animating windows have showBackdrop set to `true` during an animation, the top most window with showBackdrop set to `true` and a valid background color takes precedence.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | if a backdrop should be shown behind the animating windows. |

### getStartOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStartOffset(): Long
```

When this animation should start, relative to StartTime

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the start offset in milliseconds |

### getStartTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStartTime(): Long
```

When this animation should start. If the animation has not startet yet, this method might return `https://developer.android.com/reference/kotlin/android/view/animation/Animation#START_ON_FIRST_FRAME:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the time in milliseconds when the animation should start or `https://developer.android.com/reference/kotlin/android/view/animation/Animation#START_ON_FIRST_FRAME:kotlin.Int` |

### getTransformation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTransformation(
    currentTime: Long, 
    outTransformation: Transformation!
): Boolean
```

Gets the transformation to apply at a specified point in time. Implementations of this method should always replace the specified Transformation or document they are doing otherwise.

| Parameters ||
|---|---|
| `currentTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): Where we are in the animation. This is wall clock time. |
| `outTransformation` | [Transformation](https://developer.android.com/reference/kotlin/android/view/animation/Transformation)!: A transformation object that is provided by the caller and will be filled in by the animation. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the animation is still running |

### getTransformation

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTransformation(
    currentTime: Long, 
    outTransformation: Transformation!, 
    scale: Float
): Boolean
```

Gets the transformation to apply at a specified point in time. Implementations of this method should always replace the specified Transformation or document they are doing otherwise.

| Parameters ||
|---|---|
| `currentTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): Where we are in the animation. This is wall clock time. |
| `outTransformation` | [Transformation](https://developer.android.com/reference/kotlin/android/view/animation/Transformation)!: A transformation object that is provided by the caller and will be filled in by the animation. |
| `scale` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Scaling factor to apply to any inputs to the transform operation, such pivot points being rotated or scaled around. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the animation is still running |

### getZAdjustment

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getZAdjustment(): Int
```

Returns the Z ordering mode to use while running the animation as previously set by `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setZAdjustment(kotlin.Int)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns one of `https://developer.android.com/reference/kotlin/android/view/animation/Animation#ZORDER_NORMAL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/animation/Animation#ZORDER_TOP:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/animation/Animation#ZORDER_BOTTOM:kotlin.Int`. |

### hasEnded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasEnded(): Boolean
```

Indicates whether this animation has ended or not.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the animation has ended, false otherwise |

### hasStarted

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasStarted(): Boolean
```

Indicates whether this animation has started or not.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the animation has started, false otherwise |

### initialize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun initialize(
    width: Int, 
    height: Int, 
    parentWidth: Int, 
    parentHeight: Int
): Unit
```

Initialize this animation with the dimensions of the object being animated as well as the objects parents. (This is to support animation sizes being specified relative to these dimensions.)

Objects that interpret Animations should call this method when the sizes of the object being animated and its parent are known, and before calling #getTransformation.

| Parameters ||
|---|---|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Width of the object being animated |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Height of the object being animated |
| `parentWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Width of the animated object's parent |
| `parentHeight` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Height of the animated object's parent |

### isFillEnabled

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isFillEnabled(): Boolean
```

If fillEnabled is true, this animation will apply the value of fillBefore.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the animation will take fillBefore into account |

### isInitialized

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isInitialized(): Boolean
```

Whether or not the animation has been initialized.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Has this animation been initialized. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/animation/Animation#initialize(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reset(): Unit
```

Reset the initialization state of this animation.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/animation/Animation#initialize(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`

### restrictDuration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun restrictDuration(durationMillis: Long): Unit
```

Ensure that the duration that this animation will run is not longer than durationMillis. In addition to adjusting the duration itself, this ensures that the repeat count also will not make it run longer than the given time.

| Parameters ||
|---|---|
| `durationMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The maximum duration the animation is allowed to run. |

### scaleCurrentDuration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun scaleCurrentDuration(scale: Float): Unit
```

How much to scale the duration by.

| Parameters ||
|---|---|
| `scale` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The amount to scale the duration. |

### setAnimationListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAnimationListener(listener: Animation.AnimationListener!): Unit
```

Binds an animation listener to this animation. The animation listener is notified of animation events such as the end of the animation or the repetition of the animation.

| Parameters ||
|---|---|
| `listener` | [Animation.AnimationListener](https://developer.android.com/reference/kotlin/android/view/animation/Animation.AnimationListener)!: the animation listener to be notified |

### setBackdropColor

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBackdropColor(backdropColor: Int): Unit
```

Set the color to use for the backdrop shown behind the animating windows. Will only show the backdrop if showBackdrop was set to true. See `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setShowBackdrop(kotlin.Boolean)`.

| Parameters ||
|---|---|
| `backdropColor` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The backdrop color. If 0, the backdrop color will not apply. |

### setBackgroundColor

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBackgroundColor(bg: Int): Unit
```

**Deprecated:** *None of window animations are running with background color.*

Set background behind animation.

| Parameters ||
|---|---|
| `bg` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The background color. If 0, no background. Currently must be black, with any desired alpha level. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setBackdropColor(kotlin.Int)`

### setDetachWallpaper

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDetachWallpaper(detachWallpaper: Boolean): Unit
```

**Deprecated:** *All window animations are running with detached wallpaper.*

If detachWallpaper is true, and this is a window animation of a window that has a wallpaper background, then the window will be detached from the wallpaper while it runs. That is, the animation will only be applied to the window, and the wallpaper behind it will remain static.

| Parameters ||
|---|---|
| `detachWallpaper` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the wallpaper should be detached from the animation |

### setDuration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDuration(durationMillis: Long): Unit
```

How long this animation should last. The duration cannot be negative.

| Parameters ||
|---|---|
| `durationMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): Duration in milliseconds |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the duration is \< 0 |

### setFillAfter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFillAfter(fillAfter: Boolean): Unit
```

If fillAfter is true, the transformation that this animation performed will persist when it is finished. Defaults to false if not set. Note that this applies to individual animations and when using an `https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet` to chain animations.

| Parameters ||
|---|---|
| `fillAfter` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the animation should apply its transformation after it ends |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setFillEnabled(kotlin.Boolean)`

### setFillBefore

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFillBefore(fillBefore: Boolean): Unit
```

If fillBefore is true, this animation will apply its transformation before the start time of the animation. Defaults to true if `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setFillEnabled(kotlin.Boolean)` is not set to true. Note that this applies when using an `https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet` to chain animations. The transformation is not applied before the AnimationSet itself starts.

| Parameters ||
|---|---|
| `fillBefore` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the animation should apply its transformation before it starts |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setFillEnabled(kotlin.Boolean)`

### setFillEnabled

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFillEnabled(fillEnabled: Boolean): Unit
```

If fillEnabled is true, the animation will apply the value of fillBefore. Otherwise, fillBefore is ignored and the animation transformation is always applied until the animation ends.

| Parameters ||
|---|---|
| `fillEnabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the animation should take the value of fillBefore into account |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setFillBefore(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setFillAfter(kotlin.Boolean)`

### setInterpolator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setInterpolator(
    context: Context!, 
    resID: Int
): Unit
```

Sets the acceleration curve for this animation. The interpolator is loaded as a resource from the specified context.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: The application environment |
| `resID` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource identifier of the interpolator to load |

### setInterpolator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setInterpolator(i: Interpolator!): Unit
```

Sets the acceleration curve for this animation. Defaults to a linear interpolation.

| Parameters ||
|---|---|
| `i` | [Interpolator](https://developer.android.com/reference/kotlin/android/view/animation/Interpolator)!: The interpolator which defines the acceleration curve |

### setRepeatCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRepeatCount(repeatCount: Int): Unit
```

Sets how many times the animation should be repeated. If the repeat count is 0, the animation is never repeated. If the repeat count is greater than 0 or `https://developer.android.com/reference/kotlin/android/view/animation/Animation#INFINITE:kotlin.Int`, the repeat mode will be taken into account. The repeat count is 0 by default.

| Parameters ||
|---|---|
| `repeatCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of times the animation should be repeated |

### setRepeatMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRepeatMode(repeatMode: Int): Unit
```

Defines what this animation should do when it reaches the end. This setting is applied only when the repeat count is either greater than 0 or `https://developer.android.com/reference/kotlin/android/view/animation/Animation#INFINITE:kotlin.Int`. Defaults to `https://developer.android.com/reference/kotlin/android/view/animation/Animation#RESTART:kotlin.Int`.

| Parameters ||
|---|---|
| `repeatMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): `https://developer.android.com/reference/kotlin/android/view/animation/Animation#RESTART:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/animation/Animation#REVERSE:kotlin.Int` |

### setShowBackdrop

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setShowBackdrop(showBackdrop: Boolean): Unit
```

If showBackdrop is `true` and this animation is applied on a window, then the windows in the animation will animate with the background associated with this window behind them. If no backdrop color is explicitly set, the backdrop's color comes from the `https://developer.android.com/reference/kotlin/android/R.styleable.html#Theme_colorBackground:kotlin.Int` that is applied to this window through its theme. If multiple animating windows have showBackdrop set to `true` during an animation, the top most window with showBackdrop set to `true` and a valid background color takes precedence.

| Parameters ||
|---|---|
| `showBackdrop` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether to show a background behind the windows during the animation. |

### setStartOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStartOffset(startOffset: Long): Unit
```

When this animation should start relative to the start time. This is most useful when composing complex animations using an `https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet` where some of the animations components start at different times.

| Parameters ||
|---|---|
| `startOffset` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): When this Animation should start, in milliseconds from the start time of the root AnimationSet. |

### setStartTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStartTime(startTimeMillis: Long): Unit
```

When this animation should start. When the start time is set to `https://developer.android.com/reference/kotlin/android/view/animation/Animation#START_ON_FIRST_FRAME:kotlin.Int`, the animation will start the first time `https://developer.android.com/reference/kotlin/android/view/animation/Animation#getTransformation(kotlin.Long,%20android.view.animation.Transformation)` is invoked. The time passed to this method should be obtained by calling `https://developer.android.com/reference/kotlin/android/view/animation/AnimationUtils#currentAnimationTimeMillis()` instead of `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`.

| Parameters ||
|---|---|
| `startTimeMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the start time in milliseconds |

### setZAdjustment

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setZAdjustment(zAdjustment: Int): Unit
```

Set the Z ordering mode to use while running the animation.

| Parameters ||
|---|---|
| `zAdjustment` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired mode, one of `https://developer.android.com/reference/kotlin/android/view/animation/Animation#ZORDER_NORMAL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/animation/Animation#ZORDER_TOP:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/animation/Animation#ZORDER_BOTTOM:kotlin.Int`. |

### start

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun start(): Unit
```

Convenience method to start the animation the first time `https://developer.android.com/reference/kotlin/android/view/animation/Animation#getTransformation(kotlin.Long,%20android.view.animation.Transformation)` is invoked.

### startNow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startNow(): Unit
```

Convenience method to start the animation at the current time in milliseconds.

### willChangeBounds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun willChangeBounds(): Boolean
```

Indicates whether or not this animation will affect the bounds of the animated view. For instance, a fade animation will not affect the bounds whereas a 200% scale animation will.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this animation will change the view's bounds |

### willChangeTransformationMatrix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun willChangeTransformationMatrix(): Boolean
```

Indicates whether or not this animation will affect the transformation matrix. For instance, a fade animation will not affect the matrix whereas a scale animation will.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this animation will change the transformation matrix |

## Protected methods

### applyTransformation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun applyTransformation(
    interpolatedTime: Float, 
    t: Transformation!
): Unit
```

Helper for getTransformation. Subclasses should implement this to apply their transforms given an interpolation value. Implementations of this method should always replace the specified Transformation or document they are doing otherwise.

| Parameters ||
|---|---|
| `interpolatedTime` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The value of the normalized time (0.0 to 1.0) after it has been run through the interpolation function. |
| `t` | [Transformation](https://developer.android.com/reference/kotlin/android/view/animation/Transformation)!: The Transformation object to fill in with the current transforms. |

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun clone(): Animation
```

Creates and returns a copy of this object. The precise meaning of "copy" may depend on the class of the object. The general intent is that, for any object `x`, the expression:

```kotlin
x.clone() != x
```
will be true, and that the expression:

```kotlin
x.clone().getClass() == x.getClass()
```
will be `true`, but these are not absolute requirements. While it is typically the case that:

```kotlin
x.clone().equals(x)
```
will be `true`, this is not an absolute requirement.

<br />

By convention, the returned object should be obtained by calling `super.clone`. If a class and all of its superclasses (except `Object`) obey this convention, it will be the case that `x.clone().getClass() == x.getClass()`.

By convention, the object returned by this method should be independent of this object (which is being cloned). To achieve this independence, it may be necessary to modify one or more fields of the object returned by `super.clone` before returning it. Typically, this means copying any mutable objects that comprise the internal "deep structure" of the object being cloned and replacing the references to these objects with references to the copies. If a class contains only primitive fields or references to immutable objects, then it is usually the case that no fields in the object returned by `super.clone` need to be modified.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/animation/Animation#` | a clone of this instance. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### ensureInterpolator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun ensureInterpolator(): Unit
```

Gurantees that this animation has an interpolator. Will use a AccelerateDecelerateInterpolator is nothing else was specified.

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun finalize(): Unit
```

Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup.

The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded.

The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition.

The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates.

After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded.

The `finalize` method is never invoked more than once by a Java virtual machine for any given object.

Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored.

| Exceptions ||
|---|---|
| `java.lang.Throwable` | the `Exception` raised by this method |

### getScaleFactor

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getScaleFactor(): Float
```

The scale factor is set by the call to `getTransformation`. Overrides of `https://developer.android.com/reference/kotlin/android/view/animation/Animation#getTransformation(kotlin.Long,%20android.view.animation.Transformation,%20kotlin.Float)` will get this value directly. Overrides of `https://developer.android.com/reference/kotlin/android/view/animation/Animation#applyTransformation(kotlin.Float,%20android.view.animation.Transformation)` can call this method to get the value.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | float The scale factor that should be applied to pre-scaled values in an Animation such as the pivot points in `https://developer.android.com/reference/kotlin/android/view/animation/ScaleAnimation` and `https://developer.android.com/reference/kotlin/android/view/animation/RotateAnimation`. |

### resolveSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun resolveSize(
    type: Int, 
    value: Float, 
    size: Int, 
    parentSize: Int
): Float
```

Convert the information in the description of a size to an actual dimension

| Parameters ||
|---|---|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): One of Animation.ABSOLUTE, Animation.RELATIVE_TO_SELF, or Animation.RELATIVE_TO_PARENT. |
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The dimension associated with the type parameter |
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The size of the object being animated |
| `parentSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The size of the parent of the object being animated |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The dimension to use for the animation |
