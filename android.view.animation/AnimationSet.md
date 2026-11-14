# AnimationSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnimationSet

Kotlin| [Java](https://developer.android.com/reference/android/view/animation/AnimationSet "View this page in Java") 

```
open class AnimationSet : Animation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.view.animation.Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation) ||
| | ↳ | [android.view.animation.AnimationSet](https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet#) |

Represents a group of Animations that should be played together. The transformation of each individual animation are composed together into a single transform. If AnimationSet sets any properties that its children also set (for example, duration or fillBefore), the values of AnimationSet override the child values.

The way that AnimationSet inherits behavior from Animation is important to understand. Some of the Animation attributes applied to AnimationSet affect the AnimationSet itself, some are pushed down to the children, and some are ignored, as follows:

- duration, repeatMode, fillBefore, fillAfter: These properties, when set on an AnimationSet object, will be pushed down to all child animations.
- repeatCount, fillEnabled: These properties are ignored for AnimationSet.
- startOffset, shareInterpolator: These properties apply to the AnimationSet itself.

Starting with [android.os.Build.VERSION_CODES#ICE_CREAM_SANDWICH](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int), the behavior of these properties is the same in XML resources and at runtime (prior to that release, the values set in XML were ignored for AnimationSet). That is, calling`setDuration(500)`on an AnimationSet has the same effect as declaring`android:duration="500"`in an XML resource for an AnimationSet object.

<br />

## Summary

| Inherited constants ||
|---|---|
| From class [Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ABSOLUTE](https://developer.android.com/reference/kotlin/android/view/animation/Animation#ABSOLUTE:kotlin.Int) <br /> The specified dimension is an absolute number of pixels. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INFINITE](https://developer.android.com/reference/kotlin/android/view/animation/Animation#INFINITE:kotlin.Int) <br /> Repeat the animation indefinitely. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RELATIVE_TO_PARENT](https://developer.android.com/reference/kotlin/android/view/animation/Animation#RELATIVE_TO_PARENT:kotlin.Int) <br /> The specified dimension holds a float and should be multiplied by the height or width of the parent of the object being animated. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RELATIVE_TO_SELF](https://developer.android.com/reference/kotlin/android/view/animation/Animation#RELATIVE_TO_SELF:kotlin.Int) <br /> The specified dimension holds a float and should be multiplied by the height or width of the object being animated. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESTART](https://developer.android.com/reference/kotlin/android/view/animation/Animation#RESTART:kotlin.Int) <br /> When the animation reaches the end and the repeat count is INFINTE_REPEAT or a positive value, the animation restarts from the beginning. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REVERSE](https://developer.android.com/reference/kotlin/android/view/animation/Animation#REVERSE:kotlin.Int) <br /> When the animation reaches the end and the repeat count is INFINTE_REPEAT or a positive value, the animation plays backward (and then forward again). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [START_ON_FIRST_FRAME](https://developer.android.com/reference/kotlin/android/view/animation/Animation#START_ON_FIRST_FRAME:kotlin.Int) <br /> Can be used as the start time to indicate the start time should be the current time when [getTransformation(long,android.view.animation.Transformation)](https://developer.android.com/reference/kotlin/android/view/animation/Animation#getTransformation(kotlin.Long,%20android.view.animation.Transformation))is invoked for the first animation frame. This can is useful for short animations. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ZORDER_BOTTOM](https://developer.android.com/reference/kotlin/android/view/animation/Animation#ZORDER_BOTTOM:kotlin.Int) <br /> Requests that the content being animated be forced under all other content for the duration of the animation. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ZORDER_NORMAL](https://developer.android.com/reference/kotlin/android/view/animation/Animation#ZORDER_NORMAL:kotlin.Int) <br /> Requests that the content being animated be kept in its current Z order. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ZORDER_TOP](https://developer.android.com/reference/kotlin/android/view/animation/Animation#ZORDER_TOP:kotlin.Int) <br /> Requests that the content being animated be forced on top of all other content for the duration of the animation. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AnimationSet](https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet#AnimationSet(android.content.Context,%20android.util.AttributeSet))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!`)` Constructor used when an AnimationSet is loaded from a resource. |
| [AnimationSet](https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet#AnimationSet(kotlin.Boolean))`(`shareInterpolator:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Constructor to use when building an AnimationSet from code |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addAnimation](https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet#addAnimation(android.view.animation.Animation))`(`a:` ` [Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation)!`)` Add a child animation to this animation set. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [computeDurationHint](https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet#computeDurationHint())`()` The duration hint of an animation set is the maximum of the duration hints of all of its component animations. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation)!\>! | [getAnimations](https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet#getAnimations())`()` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDuration](https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet#getDuration())`()` The duration of an AnimationSet is defined to be the duration of the longest child animation. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartTime](https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet#getStartTime())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getTransformation](https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet#getTransformation(kotlin.Long,%20android.view.animation.Transformation))`(`currentTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `t:` ` [Transformation](https://developer.android.com/reference/kotlin/android/view/animation/Transformation)!`)` The transformation of an animation set is the concatenation of all of its component animations. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [initialize](https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet#initialize(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `parentWidth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `parentHeight:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet#reset())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restrictDuration](https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet#restrictDuration(kotlin.Long))`(`durationMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scaleCurrentDuration](https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet#scaleCurrentDuration(kotlin.Float))`(`scale:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDuration](https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet#setDuration(kotlin.Long))`(`durationMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the duration of every child animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFillAfter](https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet#setFillAfter(kotlin.Boolean))`(`fillAfter:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFillBefore](https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet#setFillBefore(kotlin.Boolean))`(`fillBefore:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRepeatMode](https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet#setRepeatMode(kotlin.Int))`(`repeatMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStartOffset](https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet#setStartOffset(kotlin.Long))`(`startOffset:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStartTime](https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet#setStartTime(kotlin.Long))`(`startTimeMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the start time of this animation and all child animations |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [willChangeBounds](https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet#willChangeBounds())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [willChangeTransformationMatrix](https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet#willChangeTransformationMatrix())`()` <br /> |

| Protected methods ||
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| open [AnimationSet](https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet#) | [clone](https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet#clone())`()` <br /> |

| Inherited functions ||
|---|---|
| From class [Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation) |-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyTransformation](https://developer.android.com/reference/kotlin/android/view/animation/Animation#applyTransformation(kotlin.Float,%20android.view.animation.Transformation))`(`interpolatedTime:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `t:` ` [Transformation](https://developer.android.com/reference/kotlin/android/view/animation/Transformation)!`)` <br /> Helper for getTransformation. Subclasses should implement this to apply their transforms given an interpolation value. Implementations of this method should always replace the specified Transformation or document they are doing otherwise. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](https://developer.android.com/reference/kotlin/android/view/animation/Animation#cancel())`()` <br /> Cancel the animation. Cancelling an animation invokes the animation listener, if set, to notify the end of the animation. If you cancel an animation manually, you must call [reset()](https://developer.android.com/reference/kotlin/android/view/animation/Animation#reset())before starting the animation again. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ensureInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/Animation#ensureInterpolator())`()` <br /> Gurantees that this animation has an interpolator. Will use a AccelerateDecelerateInterpolator is nothing else was specified. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/view/animation/Animation#finalize())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBackdropColor](https://developer.android.com/reference/kotlin/android/view/animation/Animation#getBackdropColor())`()` <br /> Returns the background color to show behind the animating windows. Will only show the background if showBackdrop was set to true. See [setShowBackdrop(boolean)](https://developer.android.com/reference/kotlin/android/view/animation/Animation#setShowBackdrop(kotlin.Boolean)). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBackgroundColor](https://developer.android.com/reference/kotlin/android/view/animation/Animation#getBackgroundColor())`()` <br /> Returns the background color behind the animation. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getDetachWallpaper](https://developer.android.com/reference/kotlin/android/view/animation/Animation#getDetachWallpaper())`()` <br /> Return value of [setDetachWallpaper(boolean)](https://developer.android.com/reference/kotlin/android/view/animation/Animation#setDetachWallpaper(kotlin.Boolean)). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFillAfter](https://developer.android.com/reference/kotlin/android/view/animation/Animation#getFillAfter())`()` <br /> If fillAfter is true, this animation will apply its transformation after the end time of the animation. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFillBefore](https://developer.android.com/reference/kotlin/android/view/animation/Animation#getFillBefore())`()` <br /> If fillBefore is true, this animation will apply its transformation before the start time of the animation. If fillBefore is false and [fillEnabled](https://developer.android.com/reference/kotlin/android/view/animation/Animation#isFillEnabled())is true, the transformation will not be applied until the start time of the animation. <br /> | | [Interpolator](https://developer.android.com/reference/kotlin/android/view/animation/Interpolator)! | [getInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/Animation#getInterpolator())`()` <br /> Gets the acceleration curve type for this animation. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRepeatCount](https://developer.android.com/reference/kotlin/android/view/animation/Animation#getRepeatCount())`()` <br /> Defines how many times the animation should repeat. The default value is 0. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRepeatMode](https://developer.android.com/reference/kotlin/android/view/animation/Animation#getRepeatMode())`()` <br /> Defines what this animation should do when it reaches the end. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getScaleFactor](https://developer.android.com/reference/kotlin/android/view/animation/Animation#getScaleFactor())`()` <br /> The scale factor is set by the call to`getTransformation`. Overrides of [getTransformation(long,android.view.animation.Transformation,float)](https://developer.android.com/reference/kotlin/android/view/animation/Animation#getTransformation(kotlin.Long,%20android.view.animation.Transformation,%20kotlin.Float))will get this value directly. Overrides of [applyTransformation(float,android.view.animation.Transformation)](https://developer.android.com/reference/kotlin/android/view/animation/Animation#applyTransformation(kotlin.Float,%20android.view.animation.Transformation))can call this method to get the value. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getShowBackdrop](https://developer.android.com/reference/kotlin/android/view/animation/Animation#getShowBackdrop())`()` <br /> If showBackdrop is`true`and this animation is applied on a window, then the windows in the animation will animate with the background associated with this window behind them. If no backdrop color is explicitly set, the backdrop's color comes from the [android.R.styleable#Theme_colorBackground](https://developer.android.com/reference/kotlin/android/R.styleable.html#Theme_colorBackground:kotlin.Int) that is applied to this window through its theme. If multiple animating windows have showBackdrop set to`true`during an animation, the top most window with showBackdrop set to`true`and a valid background color takes precedence. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartOffset](https://developer.android.com/reference/kotlin/android/view/animation/Animation#getStartOffset())`()` <br /> When this animation should start, relative to StartTime <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getTransformation](https://developer.android.com/reference/kotlin/android/view/animation/Animation#getTransformation(kotlin.Long,%20android.view.animation.Transformation,%20kotlin.Float))`(`currentTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `outTransformation:` ` [Transformation](https://developer.android.com/reference/kotlin/android/view/animation/Transformation)!`, `scale:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Gets the transformation to apply at a specified point in time. Implementations of this method should always replace the specified Transformation or document they are doing otherwise. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getZAdjustment](https://developer.android.com/reference/kotlin/android/view/animation/Animation#getZAdjustment())`()` <br /> Returns the Z ordering mode to use while running the animation as previously set by [setZAdjustment](https://developer.android.com/reference/kotlin/android/view/animation/Animation#setZAdjustment(kotlin.Int)). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasEnded](https://developer.android.com/reference/kotlin/android/view/animation/Animation#hasEnded())`()` <br /> Indicates whether this animation has ended or not. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStarted](https://developer.android.com/reference/kotlin/android/view/animation/Animation#hasStarted())`()` <br /> Indicates whether this animation has started or not. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFillEnabled](https://developer.android.com/reference/kotlin/android/view/animation/Animation#isFillEnabled())`()` <br /> If fillEnabled is true, this animation will apply the value of fillBefore. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInitialized](https://developer.android.com/reference/kotlin/android/view/animation/Animation#isInitialized())`()` <br /> Whether or not the animation has been initialized. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [resolveSize](https://developer.android.com/reference/kotlin/android/view/animation/Animation#resolveSize(kotlin.Int,%20kotlin.Float,%20kotlin.Int,%20kotlin.Int))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `parentSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Convert the information in the description of a size to an actual dimension <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAnimationListener](https://developer.android.com/reference/kotlin/android/view/animation/Animation#setAnimationListener(android.view.animation.Animation.AnimationListener))`(`listener:` ` [Animation.AnimationListener](https://developer.android.com/reference/kotlin/android/view/animation/Animation.AnimationListener)!`)` <br /> Binds an animation listener to this animation. The animation listener is notified of animation events such as the end of the animation or the repetition of the animation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBackdropColor](https://developer.android.com/reference/kotlin/android/view/animation/Animation#setBackdropColor(kotlin.Int))`(`backdropColor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set the color to use for the backdrop shown behind the animating windows. Will only show the backdrop if showBackdrop was set to true. See [setShowBackdrop(boolean)](https://developer.android.com/reference/kotlin/android/view/animation/Animation#setShowBackdrop(kotlin.Boolean)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBackgroundColor](https://developer.android.com/reference/kotlin/android/view/animation/Animation#setBackgroundColor(kotlin.Int))`(`bg:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set background behind animation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDetachWallpaper](https://developer.android.com/reference/kotlin/android/view/animation/Animation#setDetachWallpaper(kotlin.Boolean))`(`detachWallpaper:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> If detachWallpaper is true, and this is a window animation of a window that has a wallpaper background, then the window will be detached from the wallpaper while it runs. That is, the animation will only be applied to the window, and the wallpaper behind it will remain static. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFillEnabled](https://developer.android.com/reference/kotlin/android/view/animation/Animation#setFillEnabled(kotlin.Boolean))`(`fillEnabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> If fillEnabled is true, the animation will apply the value of fillBefore. Otherwise, fillBefore is ignored and the animation transformation is always applied until the animation ends. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/Animation#setInterpolator(android.content.Context,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `resID:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the acceleration curve for this animation. The interpolator is loaded as a resource from the specified context. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/Animation#setInterpolator(android.view.animation.Interpolator))`(`i:` ` [Interpolator](https://developer.android.com/reference/kotlin/android/view/animation/Interpolator)!`)` <br /> Sets the acceleration curve for this animation. Defaults to a linear interpolation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRepeatCount](https://developer.android.com/reference/kotlin/android/view/animation/Animation#setRepeatCount(kotlin.Int))`(`repeatCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets how many times the animation should be repeated. If the repeat count is 0, the animation is never repeated. If the repeat count is greater than 0 or [INFINITE](https://developer.android.com/reference/kotlin/android/view/animation/Animation#INFINITE:kotlin.Int), the repeat mode will be taken into account. The repeat count is 0 by default. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShowBackdrop](https://developer.android.com/reference/kotlin/android/view/animation/Animation#setShowBackdrop(kotlin.Boolean))`(`showBackdrop:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> If showBackdrop is`true`and this animation is applied on a window, then the windows in the animation will animate with the background associated with this window behind them. If no backdrop color is explicitly set, the backdrop's color comes from the [android.R.styleable#Theme_colorBackground](https://developer.android.com/reference/kotlin/android/R.styleable.html#Theme_colorBackground:kotlin.Int) that is applied to this window through its theme. If multiple animating windows have showBackdrop set to`true`during an animation, the top most window with showBackdrop set to`true`and a valid background color takes precedence. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setZAdjustment](https://developer.android.com/reference/kotlin/android/view/animation/Animation#setZAdjustment(kotlin.Int))`(`zAdjustment:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set the Z ordering mode to use while running the animation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](https://developer.android.com/reference/kotlin/android/view/animation/Animation#start())`()` <br /> Convenience method to start the animation the first time [getTransformation(long,android.view.animation.Transformation)](https://developer.android.com/reference/kotlin/android/view/animation/Animation#getTransformation(kotlin.Long,%20android.view.animation.Transformation))is invoked. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startNow](https://developer.android.com/reference/kotlin/android/view/animation/Animation#startNow())`()` <br /> Convenience method to start the animation at the current time in milliseconds. <br /> | ||

## Public constructors

### AnimationSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AnimationSet(
    context: Context!, 
    attrs: AttributeSet!)
```

Constructor used when an AnimationSet is loaded from a resource.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:Application context to use |
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!:Attribute set from which to read values |

### AnimationSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AnimationSet(shareInterpolator: Boolean)
```

Constructor to use when building an AnimationSet from code

| Parameters ||
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `shareInterpolator` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Pass true if all of the animations in this set should use the interpolator associated with this AnimationSet. Pass false if each animation should use its own interpolator. |

## Public methods

### addAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addAnimation(a: Animation!): Unit
```

Add a child animation to this animation set. The transforms of the child animations are applied in the order that they were added

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------|
| `a` | [Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation)!:Animation to add. |

### computeDurationHint

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun computeDurationHint(): Long
```

The duration hint of an animation set is the maximum of the duration hints of all of its component animations. 
**See Also**

- [android.view.animation.Animation#computeDurationHint](https://developer.android.com/reference/kotlin/android/view/animation/Animation#computeDurationHint()) 

### getAnimations

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAnimations(): MutableList<Animation!>!
```

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation)!>! | All the child animations in this AnimationSet. Note that this may include other AnimationSets, which are not expanded. |

### getDuration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDuration(): Long
```

The duration of an AnimationSet is defined to be the duration of the longest child animation.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the duration in milliseconds of the animation |

**See Also**

- [android.view.animation.Animation#getDuration()](https://developer.android.com/reference/kotlin/android/view/animation/Animation#getDuration()) 

### getStartTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStartTime(): Long
```

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the time in milliseconds when the animation should start or [START_ON_FIRST_FRAME](https://developer.android.com/reference/kotlin/android/view/animation/Animation#START_ON_FIRST_FRAME:kotlin.Int) |

### getTransformation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTransformation(
    currentTime: Long, 
    t: Transformation!
): Boolean
```

The transformation of an animation set is the concatenation of all of its component animations.

| Parameters ||
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `currentTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Where we are in the animation. This is wall clock time. |
| `outTransformation` | A transformation object that is provided by the caller and will be filled in by the animation. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the animation is still running |

**See Also**

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
| `parentHeight` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Height of the animated object's parent |

**See Also**

- [android.view.animation.Animation#initialize(int, int, int, int)](https://developer.android.com/reference/kotlin/android/view/animation/Animation#initialize(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)) 

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```  

### restrictDuration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun restrictDuration(durationMillis: Long): Unit
```

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `durationMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The maximum duration the animation is allowed to run. |

### scaleCurrentDuration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun scaleCurrentDuration(scale: Float): Unit
```

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------|
| `scale` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The amount to scale the duration. |

**See Also**

- [android.view.animation.Animation#scaleCurrentDuration(float)](https://developer.android.com/reference/kotlin/android/view/animation/Animation#scaleCurrentDuration(kotlin.Float)) 

### setDuration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDuration(durationMillis: Long): Unit
```

Sets the duration of every child animation.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `durationMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the duration of the animation, in milliseconds, for every child in this set |

| Exceptions ||
|--------------------------------------|-------------------------|
| `java.lang.IllegalArgumentException` | if the duration is \< 0 |

### setFillAfter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFillAfter(fillAfter: Boolean): Unit
```

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fillAfter` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the animation should apply its transformation after it ends |

### setFillBefore

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFillBefore(fillBefore: Boolean): Unit
```

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fillBefore` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the animation should apply its transformation before it starts |

### setRepeatMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRepeatMode(repeatMode: Int): Unit
```

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `repeatMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): [RESTART](https://developer.android.com/reference/kotlin/android/view/animation/Animation#RESTART:kotlin.Int) or [REVERSE](https://developer.android.com/reference/kotlin/android/view/animation/Animation#REVERSE:kotlin.Int) |

### setStartOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStartOffset(startOffset: Long): Unit
```

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `startOffset` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):When this Animation should start, in milliseconds from the start time of the root AnimationSet. |

### setStartTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStartTime(startTimeMillis: Long): Unit
```

Sets the start time of this animation and all child animations

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------|
| `startTimeMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the start time in milliseconds |

**See Also**

- [android.view.animation.Animation#setStartTime(long)](https://developer.android.com/reference/kotlin/android/view/animation/Animation#setStartTime(kotlin.Long)) 

### willChangeBounds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun willChangeBounds(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this animation will change the view's bounds |

### willChangeTransformationMatrix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun willChangeTransformationMatrix(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this animation will change the transformation matrix |

## Protected methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun clone(): AnimationSet
```

| Return ||
|-----------------------------------------------------------------------------------------------------|---------------------------|
| [AnimationSet](https://developer.android.com/reference/kotlin/android/view/animation/AnimationSet#) | a clone of this instance. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |
