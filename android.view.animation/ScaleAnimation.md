# ScaleAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScaleAnimation

Kotlin| [Java](ScaleAnimation.md) 
| --- | --- |

```
open class ScaleAnimation : Animation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.view.animation.Animation](Animation.md) ||
| | ↳ | [android.view.animation.ScaleAnimation](ScaleAnimation.md) |

An animation that controls the scale of an object. You can specify the point to use for the center of scaling.

## Summary

| Inherited constants ||
|---|---|
| From class [Animation](Animation.md) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ABSOLUTE](Animation.md) <br /> The specified dimension is an absolute number of pixels. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INFINITE](Animation.md) <br /> Repeat the animation indefinitely. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RELATIVE_TO_PARENT](Animation.md) <br /> The specified dimension holds a float and should be multiplied by the height or width of the parent of the object being animated. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RELATIVE_TO_SELF](Animation.md) <br /> The specified dimension holds a float and should be multiplied by the height or width of the object being animated. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESTART](Animation.md) <br /> When the animation reaches the end and the repeat count is INFINTE_REPEAT or a positive value, the animation restarts from the beginning. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REVERSE](Animation.md) <br /> When the animation reaches the end and the repeat count is INFINTE_REPEAT or a positive value, the animation plays backward (and then forward again). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [START_ON_FIRST_FRAME](Animation.md) <br /> Can be used as the start time to indicate the start time should be the current time when [getTransformation(long,android.view.animation.Transformation)](Animation.md))is invoked for the first animation frame. This can is useful for short animations. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ZORDER_BOTTOM](Animation.md) <br /> Requests that the content being animated be forced under all other content for the duration of the animation. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ZORDER_NORMAL](Animation.md) <br /> Requests that the content being animated be kept in its current Z order. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ZORDER_TOP](Animation.md) <br /> Requests that the content being animated be forced on top of all other content for the duration of the animation. <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ScaleAnimation](ScaleAnimation.md))`(`context:` ` [Context](../android.content/Context.md)!`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)!`)` Constructor used when a ScaleAnimation is loaded from a resource. |
| [ScaleAnimation](ScaleAnimation.md))`(`fromX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `toX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `fromY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `toY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Constructor to use when building a ScaleAnimation from code |
| [ScaleAnimation](ScaleAnimation.md))`(`fromX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `toX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `fromY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `toY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `pivotX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `pivotY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Constructor to use when building a ScaleAnimation from code |
| [ScaleAnimation](ScaleAnimation.md))`(`fromX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `toX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `fromY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `toY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `pivotXType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pivotXValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `pivotYType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pivotYValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Constructor to use when building a ScaleAnimation from code |

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [initialize](ScaleAnimation.md))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `parentWidth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `parentHeight:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyTransformation](ScaleAnimation.md))`(`interpolatedTime:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `t:` ` [Transformation](Transformation.md)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [Animation](Animation.md) |-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](Animation.md))`()` <br /> Cancel the animation. Cancelling an animation invokes the animation listener, if set, to notify the end of the animation. If you cancel an animation manually, you must call [reset()](Animation.md))before starting the animation again. <br /> | | [Animation](Animation.md) | [clone](Animation.md))`()` <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [computeDurationHint](Animation.md))`()` <br /> Compute a hint at how long the entire animation may last, in milliseconds. Animations can be written to cause themselves to run for a different duration than what is computed here, but generally this should be accurate. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ensureInterpolator](Animation.md))`()` <br /> Gurantees that this animation has an interpolator. Will use a AccelerateDecelerateInterpolator is nothing else was specified. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](Animation.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBackdropColor](Animation.md))`()` <br /> Returns the background color to show behind the animating windows. Will only show the background if showBackdrop was set to true. See [setShowBackdrop(boolean)](Animation.md)). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBackgroundColor](Animation.md))`()` <br /> Returns the background color behind the animation. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getDetachWallpaper](Animation.md))`()` <br /> Return value of [setDetachWallpaper(boolean)](Animation.md)). <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDuration](Animation.md))`()` <br /> How long this animation should last <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFillAfter](Animation.md))`()` <br /> If fillAfter is true, this animation will apply its transformation after the end time of the animation. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFillBefore](Animation.md))`()` <br /> If fillBefore is true, this animation will apply its transformation before the start time of the animation. If fillBefore is false and [fillEnabled](Animation.md))is true, the transformation will not be applied until the start time of the animation. <br /> | | [Interpolator](Interpolator.md)! | [getInterpolator](Animation.md))`()` <br /> Gets the acceleration curve type for this animation. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRepeatCount](Animation.md))`()` <br /> Defines how many times the animation should repeat. The default value is 0. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRepeatMode](Animation.md))`()` <br /> Defines what this animation should do when it reaches the end. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getScaleFactor](Animation.md))`()` <br /> The scale factor is set by the call to`getTransformation`. Overrides of [getTransformation(long,android.view.animation.Transformation,float)](Animation.md))will get this value directly. Overrides of [applyTransformation(float,android.view.animation.Transformation)](Animation.md))can call this method to get the value. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getShowBackdrop](Animation.md))`()` <br /> If showBackdrop is`true`and this animation is applied on a window, then the windows in the animation will animate with the background associated with this window behind them. If no backdrop color is explicitly set, the backdrop's color comes from the [android.R.styleable#Theme_colorBackground](../android/R.styleable.md) that is applied to this window through its theme. If multiple animating windows have showBackdrop set to`true`during an animation, the top most window with showBackdrop set to`true`and a valid background color takes precedence. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartOffset](Animation.md))`()` <br /> When this animation should start, relative to StartTime <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartTime](Animation.md))`()` <br /> When this animation should start. If the animation has not startet yet, this method might return [START_ON_FIRST_FRAME](Animation.md). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getTransformation](Animation.md))`(`currentTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `outTransformation:` ` [Transformation](Transformation.md)!`)` <br /> Gets the transformation to apply at a specified point in time. Implementations of this method should always replace the specified Transformation or document they are doing otherwise. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getTransformation](Animation.md))`(`currentTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `outTransformation:` ` [Transformation](Transformation.md)!`, `scale:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Gets the transformation to apply at a specified point in time. Implementations of this method should always replace the specified Transformation or document they are doing otherwise. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getZAdjustment](Animation.md))`()` <br /> Returns the Z ordering mode to use while running the animation as previously set by [setZAdjustment](Animation.md)). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasEnded](Animation.md))`()` <br /> Indicates whether this animation has ended or not. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStarted](Animation.md))`()` <br /> Indicates whether this animation has started or not. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFillEnabled](Animation.md))`()` <br /> If fillEnabled is true, this animation will apply the value of fillBefore. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInitialized](Animation.md))`()` <br /> Whether or not the animation has been initialized. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](Animation.md))`()` <br /> Reset the initialization state of this animation. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [resolveSize](Animation.md))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `parentSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Convert the information in the description of a size to an actual dimension <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restrictDuration](Animation.md))`(`durationMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Ensure that the duration that this animation will run is not longer than durationMillis. In addition to adjusting the duration itself, this ensures that the repeat count also will not make it run longer than the given time. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scaleCurrentDuration](Animation.md))`(`scale:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> How much to scale the duration by. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAnimationListener](Animation.md))`(`listener:` ` [Animation.AnimationListener](../android/view/animation/Animation.AnimationListener.md)!`)` <br /> Binds an animation listener to this animation. The animation listener is notified of animation events such as the end of the animation or the repetition of the animation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBackdropColor](Animation.md))`(`backdropColor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set the color to use for the backdrop shown behind the animating windows. Will only show the backdrop if showBackdrop was set to true. See [setShowBackdrop(boolean)](Animation.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBackgroundColor](Animation.md))`(`bg:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set background behind animation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDetachWallpaper](Animation.md))`(`detachWallpaper:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> If detachWallpaper is true, and this is a window animation of a window that has a wallpaper background, then the window will be detached from the wallpaper while it runs. That is, the animation will only be applied to the window, and the wallpaper behind it will remain static. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDuration](Animation.md))`(`durationMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> How long this animation should last. The duration cannot be negative. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFillAfter](Animation.md))`(`fillAfter:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> If fillAfter is true, the transformation that this animation performed will persist when it is finished. Defaults to false if not set. Note that this applies to individual animations and when using an to chain animations. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFillBefore](Animation.md))`(`fillBefore:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> If fillBefore is true, this animation will apply its transformation before the start time of the animation. Defaults to true if [setFillEnabled(boolean)](Animation.md))is not set to true. Note that this applies when using an to chain animations. The transformation is not applied before the AnimationSet itself starts. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFillEnabled](Animation.md))`(`fillEnabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> If fillEnabled is true, the animation will apply the value of fillBefore. Otherwise, fillBefore is ignored and the animation transformation is always applied until the animation ends. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInterpolator](Animation.md))`(`context:` ` [Context](../android.content/Context.md)!`, `resID:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the acceleration curve for this animation. The interpolator is loaded as a resource from the specified context. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInterpolator](Animation.md))`(`i:` ` [Interpolator](Interpolator.md)!`)` <br /> Sets the acceleration curve for this animation. Defaults to a linear interpolation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRepeatCount](Animation.md))`(`repeatCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets how many times the animation should be repeated. If the repeat count is 0, the animation is never repeated. If the repeat count is greater than 0 or [INFINITE](Animation.md), the repeat mode will be taken into account. The repeat count is 0 by default. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRepeatMode](Animation.md))`(`repeatMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Defines what this animation should do when it reaches the end. This setting is applied only when the repeat count is either greater than 0 or [INFINITE](Animation.md). Defaults to [RESTART](Animation.md). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShowBackdrop](Animation.md))`(`showBackdrop:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> If showBackdrop is`true`and this animation is applied on a window, then the windows in the animation will animate with the background associated with this window behind them. If no backdrop color is explicitly set, the backdrop's color comes from the [android.R.styleable#Theme_colorBackground](../android/R.styleable.md) that is applied to this window through its theme. If multiple animating windows have showBackdrop set to`true`during an animation, the top most window with showBackdrop set to`true`and a valid background color takes precedence. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStartOffset](Animation.md))`(`startOffset:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> When this animation should start relative to the start time. This is most useful when composing complex animations using an [AnimationSet](AnimationSet.md) where some of the animations components start at different times. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStartTime](Animation.md))`(`startTimeMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> When this animation should start. When the start time is set to [START_ON_FIRST_FRAME](Animation.md), the animation will start the first time [getTransformation(long,android.view.animation.Transformation)](Animation.md))is invoked. The time passed to this method should be obtained by calling [AnimationUtils.currentAnimationTimeMillis()](AnimationUtils.md))instead of [System.currentTimeMillis()](../java.lang/System.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setZAdjustment](Animation.md))`(`zAdjustment:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set the Z ordering mode to use while running the animation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](Animation.md))`()` <br /> Convenience method to start the animation the first time [getTransformation(long,android.view.animation.Transformation)](Animation.md))is invoked. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startNow](Animation.md))`()` <br /> Convenience method to start the animation at the current time in milliseconds. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [willChangeBounds](Animation.md))`()` <br /> Indicates whether or not this animation will affect the bounds of the animated view. For instance, a fade animation will not affect the bounds whereas a 200% scale animation will. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [willChangeTransformationMatrix](Animation.md))`()` <br /> Indicates whether or not this animation will affect the transformation matrix. For instance, a fade animation will not affect the matrix whereas a scale animation will. <br /> | ||

## Public constructors

### ScaleAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ScaleAnimation(
    context: Context!, 
    attrs: AttributeSet!)
```

Constructor used when a ScaleAnimation is loaded from a resource.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:Application context to use |
| `attrs` | [AttributeSet](../android.util/AttributeSet.md)!:Attribute set from which to read values |

### ScaleAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ScaleAnimation(
    fromX: Float, 
    toX: Float, 
    fromY: Float, 
    toY: Float)
```

Constructor to use when building a ScaleAnimation from code

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `fromX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Horizontal scaling factor to apply at the start of the animation |
| `toX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Horizontal scaling factor to apply at the end of the animation |
| `fromY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Vertical scaling factor to apply at the start of the animation |
| --- | --- |
| `toY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Vertical scaling factor to apply at the end of the animation |

### ScaleAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ScaleAnimation(
    fromX: Float, 
    toX: Float, 
    fromY: Float, 
    toY: Float, 
    pivotX: Float, 
    pivotY: Float)
```

Constructor to use when building a ScaleAnimation from code

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fromX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Horizontal scaling factor to apply at the start of the animation |
| `toX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Horizontal scaling factor to apply at the end of the animation |
| `fromY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Vertical scaling factor to apply at the start of the animation |
| --- | --- |
| `toY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Vertical scaling factor to apply at the end of the animation |
| `pivotX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The X coordinate of the point about which the object is being scaled, specified as an absolute number where 0 is the left edge. (This point remains fixed while the object changes size.) |
| `pivotY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The Y coordinate of the point about which the object is being scaled, specified as an absolute number where 0 is the top edge. (This point remains fixed while the object changes size.) |
| --- | --- |

### ScaleAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ScaleAnimation(
    fromX: Float, 
    toX: Float, 
    fromY: Float, 
    toY: Float, 
    pivotXType: Int, 
    pivotXValue: Float, 
    pivotYType: Int, 
    pivotYValue: Float)
```

Constructor to use when building a ScaleAnimation from code

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fromX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Horizontal scaling factor to apply at the start of the animation |
| `toX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Horizontal scaling factor to apply at the end of the animation |
| `fromY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Vertical scaling factor to apply at the start of the animation |
| --- | --- |
| `toY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Vertical scaling factor to apply at the end of the animation |
| `pivotXType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Specifies how pivotXValue should be interpreted. One of Animation.ABSOLUTE, Animation.RELATIVE_TO_SELF, or Animation.RELATIVE_TO_PARENT. |
| `pivotXValue` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The X coordinate of the point about which the object is being scaled, specified as an absolute number where 0 is the left edge. (This point remains fixed while the object changes size.) This value can either be an absolute number if pivotXType is ABSOLUTE, or a percentage (where 1.0 is 100%) otherwise. |
| --- | --- |
| `pivotYType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Specifies how pivotYValue should be interpreted. One of Animation.ABSOLUTE, Animation.RELATIVE_TO_SELF, or Animation.RELATIVE_TO_PARENT. |
| `pivotYValue` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The Y coordinate of the point about which the object is being scaled, specified as an absolute number where 0 is the top edge. (This point remains fixed while the object changes size.) This value can either be an absolute number if pivotYType is ABSOLUTE, or a percentage (where 1.0 is 100%) otherwise. |

## Public methods

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

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Width of the object being animated |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Height of the object being animated |
| `parentWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Width of the animated object's parent |
| --- | --- |
| `parentHeight` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Height of the animated object's parent |

## Protected methods

### applyTransformation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun applyTransformation(
    interpolatedTime: Float, 
    t: Transformation!
): Unit
```

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `interpolatedTime` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The value of the normalized time (0.0 to 1.0) after it has been run through the interpolation function. |
| `t` | [Transformation](Transformation.md)!:The Transformation object to fill in with the current transforms. |
