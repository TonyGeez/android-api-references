# android.animation

# android.animation

Kotlin| [Java](https://developer.android.com/reference/android/animation/package-summary "View this page in Java")
| --- | --- |

## Interfaces

| [AnimatorListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener) | An animation listener receives notifications from an animation. |
| --- | --- |
| [AnimatorPauseListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorPauseListener) | A pause listener receives notifications from an animation when the animation is [paused](https://developer.android.com/reference/kotlin/android/animation/Animator#pause())or [resumed](https://developer.android.com/reference/kotlin/android/animation/Animator#resume()). |
| [TransitionListener](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition.TransitionListener) | This interface is used for listening to starting and ending events for transitions. |
| [TimeListener](https://developer.android.com/reference/kotlin/android/animation/TimeAnimator.TimeListener) | Implementors of this interface can set themselves as update listeners to a`TimeAnimator`instance to receive callbacks on every animation frame to receive the total time since the animator started and the delta time since the last frame. |
| --- | --- |
| [TimeInterpolator](https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator) | A time interpolator defines the rate of change of an animation. |
| [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator) | Interface for use with the [ValueAnimator.setEvaluator(TypeEvaluator)](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#setEvaluator(android.animation.TypeEvaluator))function. |
| [AnimatorUpdateListener](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator.AnimatorUpdateListener) | Implementors of this interface can add themselves as update listeners to an`ValueAnimator`instance to receive callbacks on every animation frame, after the current frame's values have been calculated for that`ValueAnimator`. |
| --- | --- |
| [DurationScaleChangeListener](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator.DurationScaleChangeListener) | Listener interface for the system-wide scaling factor for Animator-based animations. |

## Classes

| [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator) | This is the superclass for classes which provide basic support for animations which can be started, ended, and have`AnimatorListeners`added to them. |
| --- | --- |
| [AnimatorInflater](https://developer.android.com/reference/kotlin/android/animation/AnimatorInflater) | This class is used to instantiate animator XML files into Animator objects. |
| [AnimatorListenerAdapter](https://developer.android.com/reference/kotlin/android/animation/AnimatorListenerAdapter) | This adapter class provides empty implementations of the methods from [android.animation.Animator.AnimatorListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener). |
| [AnimatorSet](https://developer.android.com/reference/kotlin/android/animation/AnimatorSet) | This class plays a set of [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator) objects in the specified order. |
| --- | --- |
| [ArgbEvaluator](https://developer.android.com/reference/kotlin/android/animation/ArgbEvaluator) | This evaluator can be used to perform type interpolation between integer values that represent ARGB colors. |
| [BidirectionalTypeConverter](https://developer.android.com/reference/kotlin/android/animation/BidirectionalTypeConverter) | Abstract base class used convert type T to another type V and back again. |
| [FloatArrayEvaluator](https://developer.android.com/reference/kotlin/android/animation/FloatArrayEvaluator) | This evaluator can be used to perform type interpolation between`float[]`values. |
| --- | --- |
| [FloatEvaluator](https://developer.android.com/reference/kotlin/android/animation/FloatEvaluator) | This evaluator can be used to perform type interpolation between`float`values. |
| [IntArrayEvaluator](https://developer.android.com/reference/kotlin/android/animation/IntArrayEvaluator) | This evaluator can be used to perform type interpolation between`int[]`values. |
| [IntEvaluator](https://developer.android.com/reference/kotlin/android/animation/IntEvaluator) | This evaluator can be used to perform type interpolation between`int`values. |
| --- | --- |
| [Keyframe](https://developer.android.com/reference/kotlin/android/animation/Keyframe) | This class holds a time/value pair for an animation. |
| [LayoutTransition](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition) | This class enables automatic animations on layout changes in ViewGroup objects. |
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator) | This subclass of [ValueAnimator](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator) provides support for animating properties on target objects. |
| --- | --- |
| [PointFEvaluator](https://developer.android.com/reference/kotlin/android/animation/PointFEvaluator) | This evaluator can be used to perform type interpolation between`PointF`values. |
| [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder) | This class holds information about a property and the values that that property should take on during an animation. |
| [RectEvaluator](https://developer.android.com/reference/kotlin/android/animation/RectEvaluator) | This evaluator can be used to perform type interpolation between`Rect`values. |
| --- | --- |
| [StateListAnimator](https://developer.android.com/reference/kotlin/android/animation/StateListAnimator) | Lets you define a number of Animators that will run on the attached View depending on the View's drawable state. |
| [TimeAnimator](https://developer.android.com/reference/kotlin/android/animation/TimeAnimator) | This class provides a simple callback mechanism to listeners that is synchronized with all other animators in the system. |
| [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter) | Abstract base class used convert type T to another type V. |
| --- | --- |
| [ValueAnimator](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator) | This class provides a simple timing engine for running animations which calculate animated values and set them on target objects. |
