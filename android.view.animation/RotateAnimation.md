Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RotateAnimation

Kotlin | [Java](RotateAnimation.md)
| --- | --- |

```
open class RotateAnimation : Animation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.view.animation.Animation](Animation.md) ||
| | ↳ | [android.view.animation.RotateAnimation](RotateAnimation.md) |

An animation that controls the rotation of an object. This rotation takes place in the X-Y plane. You can specify the point to use for the center of the rotation, where (0,0) is the top left point. If not specified, (0,0) is the default rotation point.

## Summary

| Inherited constants ||
|---|---|
| From class Animation |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#ABSOLUTE:kotlin.Int` The specified dimension is an absolute number of pixels. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#INFINITE:kotlin.Int` Repeat the animation indefinitely. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#RELATIVE_TO_PARENT:kotlin.Int` The specified dimension holds a float and should be multiplied by the height or width of the parent of the object being animated. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#RELATIVE_TO_SELF:kotlin.Int` The specified dimension holds a float and should be multiplied by the height or width of the object being animated. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#RESTART:kotlin.Int` When the animation reaches the end and the repeat count is INFINTE_REPEAT or a positive value, the animation restarts from the beginning. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#REVERSE:kotlin.Int` When the animation reaches the end and the repeat count is INFINTE_REPEAT or a positive value, the animation plays backward (and then forward again). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#START_ON_FIRST_FRAME:kotlin.Int` Can be used as the start time to indicate the start time should be the current time when getTransformation is invoked for the first animation frame. This can is useful for short animations. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#ZORDER_BOTTOM:kotlin.Int` Requests that the content being animated be forced under all other content for the duration of the animation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#ZORDER_NORMAL:kotlin.Int` Requests that the content being animated be kept in its current Z order. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/view/animation/Animation#ZORDER_TOP:kotlin.Int` Requests that the content being animated be forced on top of all other content for the duration of the animation. <br /> | ||

| Public constructors ||
|---|---|
| RotateAnimation Constructor used when a RotateAnimation is loaded from a resource. |
| RotateAnimation Constructor to use when building a RotateAnimation from code. |
| RotateAnimation Constructor to use when building a RotateAnimation from code |
| RotateAnimation Constructor to use when building a RotateAnimation from code |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | initialize Initialize this animation with the dimensions of the object being animated as well as the objects parents. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | applyTransformation Helper for getTransformation. |

| Inherited functions ||
|---|---|
| From class Animation |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | cancel Cancel the animation. Cancelling an animation invokes the animation listener, if set, to notify the end of the animation. If you cancel an animation manually, you must call reset before starting the animation again. <br /> | | Animation | clone Creates and returns a copy of this object. The precise meaning of "copy" may depend on the class of the object. The general intent is that, for any object `x`, the expression: ```kotlin x.clone() != x ``` will be true, and that the expression: ```kotlin x.clone().getClass() == x.getClass() ``` will be `true`, but these are not absolute requirements. While it is typically the case that: ```kotlin x.clone().equals(x) ``` will be `true`, this is not an absolute requirement. <br /> By convention, the returned object should be obtained by calling `super.clone`. If a class and all of its superclasses (except `Object`) obey this convention, it will be the case that `x.clone().getClass() == x.getClass()`. By convention, the object returned by this method should be independent of this object (which is being cloned). To achieve this independence, it may be necessary to modify one or more fields of the object returned by `super.clone` before returning it. Typically, this means copying any mutable objects that comprise the internal "deep structure" of the object being cloned and replacing the references to these objects with references to the copies. If a class contains only primitive fields or references to immutable objects, then it is usually the case that no fields in the object returned by `super.clone` need to be modified. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | computeDurationHint Compute a hint at how long the entire animation may last, in milliseconds. Animations can be written to cause themselves to run for a different duration than what is computed here, but generally this should be accurate. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | ensureInterpolator Gurantees that this animation has an interpolator. Will use a AccelerateDecelerateInterpolator is nothing else was specified. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | finalize Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup. The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded. The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition. The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates. After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded. The `finalize` method is never invoked more than once by a Java virtual machine for any given object. Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getBackdropColor Returns the background color to show behind the animating windows. Will only show the background if showBackdrop was set to true. See setShowBackdrop. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getBackgroundColor Returns the background color behind the animation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getDetachWallpaper Return value of setDetachWallpaper. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | getDuration How long this animation should last <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getFillAfter If fillAfter is true, this animation will apply its transformation after the end time of the animation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getFillBefore If fillBefore is true, this animation will apply its transformation before the start time of the animation. If fillBefore is false and isFillEnabled is true, the transformation will not be applied until the start time of the animation. <br /> | | `https://developer.android.com/reference/kotlin/android/view/animation/Interpolator!` | getInterpolator Gets the acceleration curve type for this animation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getRepeatCount Defines how many times the animation should repeat. The default value is 0. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getRepeatMode Defines what this animation should do when it reaches the end. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | getScaleFactor The scale factor is set by the call to `getTransformation`. Overrides of getTransformation will get this value directly. Overrides of applyTransformation can call this method to get the value. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getShowBackdrop If showBackdrop is `true` and this animation is applied on a window, then the windows in the animation will animate with the background associated with this window behind them. If no backdrop color is explicitly set, the backdrop's color comes from the `https://developer.android.com/reference/kotlin/android/R.styleable.html#Theme_colorBackground:kotlin.Int` that is applied to this window through its theme. If multiple animating windows have showBackdrop set to `true` during an animation, the top most window with showBackdrop set to `true` and a valid background color takes precedence. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | getStartOffset When this animation should start, relative to StartTime <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | getStartTime When this animation should start. If the animation has not startet yet, this method might return `https://developer.android.com/reference/kotlin/android/view/animation/Animation#START_ON_FIRST_FRAME:kotlin.Int`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getTransformation Gets the transformation to apply at a specified point in time. Implementations of this method should always replace the specified Transformation or document they are doing otherwise. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getTransformation Gets the transformation to apply at a specified point in time. Implementations of this method should always replace the specified Transformation or document they are doing otherwise. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getZAdjustment Returns the Z ordering mode to use while running the animation as previously set by setZAdjustment. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | hasEnded Indicates whether this animation has ended or not. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | hasStarted Indicates whether this animation has started or not. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isFillEnabled If fillEnabled is true, this animation will apply the value of fillBefore. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isInitialized Whether or not the animation has been initialized. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | reset Reset the initialization state of this animation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | resolveSize Convert the information in the description of a size to an actual dimension <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | restrictDuration Ensure that the duration that this animation will run is not longer than durationMillis. In addition to adjusting the duration itself, this ensures that the repeat count also will not make it run longer than the given time. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | scaleCurrentDuration How much to scale the duration by. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setAnimationListener Binds an animation listener to this animation. The animation listener is notified of animation events such as the end of the animation or the repetition of the animation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setBackdropColor Set the color to use for the backdrop shown behind the animating windows. Will only show the backdrop if showBackdrop was set to true. See setShowBackdrop. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setBackgroundColor Set background behind animation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setDetachWallpaper If detachWallpaper is true, and this is a window animation of a window that has a wallpaper background, then the window will be detached from the wallpaper while it runs. That is, the animation will only be applied to the window, and the wallpaper behind it will remain static. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setDuration How long this animation should last. The duration cannot be negative. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setFillAfter If fillAfter is true, the transformation that this animation performed will persist when it is finished. Defaults to false if not set. Note that this applies to individual animations and when using an AnimationSet to chain animations. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setFillBefore If fillBefore is true, this animation will apply its transformation before the start time of the animation. Defaults to true if setFillEnabled is not set to true. Note that this applies when using an AnimationSet to chain animations. The transformation is not applied before the AnimationSet itself starts. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setFillEnabled If fillEnabled is true, the animation will apply the value of fillBefore. Otherwise, fillBefore is ignored and the animation transformation is always applied until the animation ends. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setInterpolator Sets the acceleration curve for this animation. The interpolator is loaded as a resource from the specified context. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setInterpolator Sets the acceleration curve for this animation. Defaults to a linear interpolation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setRepeatCount Sets how many times the animation should be repeated. If the repeat count is 0, the animation is never repeated. If the repeat count is greater than 0 or `https://developer.android.com/reference/kotlin/android/view/animation/Animation#INFINITE:kotlin.Int`, the repeat mode will be taken into account. The repeat count is 0 by default. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setRepeatMode Defines what this animation should do when it reaches the end. This setting is applied only when the repeat count is either greater than 0 or `https://developer.android.com/reference/kotlin/android/view/animation/Animation#INFINITE:kotlin.Int`. Defaults to `https://developer.android.com/reference/kotlin/android/view/animation/Animation#RESTART:kotlin.Int`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setShowBackdrop If showBackdrop is `true` and this animation is applied on a window, then the windows in the animation will animate with the background associated with this window behind them. If no backdrop color is explicitly set, the backdrop's color comes from the `https://developer.android.com/reference/kotlin/android/R.styleable.html#Theme_colorBackground:kotlin.Int` that is applied to this window through its theme. If multiple animating windows have showBackdrop set to `true` during an animation, the top most window with showBackdrop set to `true` and a valid background color takes precedence. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setStartOffset When this animation should start relative to the start time. This is most useful when composing complex animations using an AnimationSet where some of the animations components start at different times. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setStartTime When this animation should start. When the start time is set to `https://developer.android.com/reference/kotlin/android/view/animation/Animation#START_ON_FIRST_FRAME:kotlin.Int`, the animation will start the first time getTransformation is invoked. The time passed to this method should be obtained by calling currentAnimationTimeMillis instead of currentTimeMillis. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setZAdjustment Set the Z ordering mode to use while running the animation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | start Convenience method to start the animation the first time getTransformation is invoked. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | startNow Convenience method to start the animation at the current time in milliseconds. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | willChangeBounds Indicates whether or not this animation will affect the bounds of the animated view. For instance, a fade animation will not affect the bounds whereas a 200% scale animation will. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | willChangeTransformationMatrix Indicates whether or not this animation will affect the transformation matrix. For instance, a fade animation will not affect the matrix whereas a scale animation will. <br /> | ||

## Public constructors

### RotateAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RotateAnimation(
    context: Context!, 
    attrs: AttributeSet!)
```

Constructor used when a RotateAnimation is loaded from a resource.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md)!: Application context to use |
| `attrs` | [AttributeSet](../android.util/AttributeSet.md)!: Attribute set from which to read values |

### RotateAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RotateAnimation(
    fromDegrees: Float, 
    toDegrees: Float)
```

Constructor to use when building a RotateAnimation from code. Default pivotX/pivotY point is (0,0).

| Parameters ||
|---|---|
| `fromDegrees` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Rotation offset to apply at the start of the animation. |
| `toDegrees` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Rotation offset to apply at the end of the animation. |

### RotateAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RotateAnimation(
    fromDegrees: Float, 
    toDegrees: Float, 
    pivotX: Float, 
    pivotY: Float)
```

Constructor to use when building a RotateAnimation from code

| Parameters ||
|---|---|
| `fromDegrees` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Rotation offset to apply at the start of the animation. |
| `toDegrees` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Rotation offset to apply at the end of the animation. |
| `pivotX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The X coordinate of the point about which the object is being rotated, specified as an absolute number where 0 is the left edge. |
| --- | --- |
| `pivotY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The Y coordinate of the point about which the object is being rotated, specified as an absolute number where 0 is the top edge. |

### RotateAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RotateAnimation(
    fromDegrees: Float, 
    toDegrees: Float, 
    pivotXType: Int, 
    pivotXValue: Float, 
    pivotYType: Int, 
    pivotYValue: Float)
```

Constructor to use when building a RotateAnimation from code

| Parameters ||
|---|---|
| `fromDegrees` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Rotation offset to apply at the start of the animation. |
| `toDegrees` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Rotation offset to apply at the end of the animation. |
| `pivotXType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies how pivotXValue should be interpreted. One of Animation.ABSOLUTE, Animation.RELATIVE_TO_SELF, or Animation.RELATIVE_TO_PARENT. |
| --- | --- |
| `pivotXValue` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The X coordinate of the point about which the object is being rotated, specified as an absolute number where 0 is the left edge. This value can either be an absolute number if pivotXType is ABSOLUTE, or a percentage (where 1.0 is 100%) otherwise. |
| `pivotYType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies how pivotYValue should be interpreted. One of Animation.ABSOLUTE, Animation.RELATIVE_TO_SELF, or Animation.RELATIVE_TO_PARENT. |
| `pivotYValue` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The Y coordinate of the point about which the object is being rotated, specified as an absolute number where 0 is the top edge. This value can either be an absolute number if pivotYType is ABSOLUTE, or a percentage (where 1.0 is 100%) otherwise. |
| --- | --- |

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

Initialize this animation with the dimensions of the object being animated as well as the objects parents. (This is to support animation sizes being specified relative to these dimensions.)

Objects that interpret Animations should call this method when the sizes of the object being animated and its parent are known, and before calling #getTransformation.

| Parameters ||
|---|---|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Width of the object being animated |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Height of the object being animated |
| `parentWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Width of the animated object's parent |
| --- | --- |
| `parentHeight` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Height of the animated object's parent |

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
| `t` | [Transformation](Transformation.md)!: The Transformation object to fill in with the current transforms. |
