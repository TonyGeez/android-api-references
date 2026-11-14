# android.animation

# android.animation

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [AnimatorListener](../android/animation/Animator.AnimatorListener.md) | An animation listener receives notifications from an animation. |
| --- | --- |
| [AnimatorPauseListener](../android/animation/Animator.AnimatorPauseListener.md) | A pause listener receives notifications from an animation when the animation is [paused](Animator.md))or [resumed](Animator.md)). |
| [TransitionListener](../android/animation/LayoutTransition.TransitionListener.md) | This interface is used for listening to starting and ending events for transitions. |
| [TimeListener](../android/animation/TimeAnimator.TimeListener.md) | Implementors of this interface can set themselves as update listeners to a`TimeAnimator`instance to receive callbacks on every animation frame to receive the total time since the animator started and the delta time since the last frame. |
| --- | --- |
| [TimeInterpolator](TimeInterpolator.md) | A time interpolator defines the rate of change of an animation. |
| [TypeEvaluator](TypeEvaluator.md) | Interface for use with the [ValueAnimator.setEvaluator(TypeEvaluator)](ValueAnimator.md))function. |
| [AnimatorUpdateListener](../android/animation/ValueAnimator.AnimatorUpdateListener.md) | Implementors of this interface can add themselves as update listeners to an`ValueAnimator`instance to receive callbacks on every animation frame, after the current frame's values have been calculated for that`ValueAnimator`. |
| --- | --- |
| [DurationScaleChangeListener](../android/animation/ValueAnimator.DurationScaleChangeListener.md) | Listener interface for the system-wide scaling factor for Animator-based animations. |

## Classes

| [Animator](Animator.md) | This is the superclass for classes which provide basic support for animations which can be started, ended, and have`AnimatorListeners`added to them. |
| --- | --- |
| [AnimatorInflater](AnimatorInflater.md) | This class is used to instantiate animator XML files into Animator objects. |
| [AnimatorListenerAdapter](AnimatorListenerAdapter.md) | This adapter class provides empty implementations of the methods from [android.animation.Animator.AnimatorListener](../android/animation/Animator.AnimatorListener.md). |
| [AnimatorSet](AnimatorSet.md) | This class plays a set of [Animator](Animator.md) objects in the specified order. |
| --- | --- |
| [ArgbEvaluator](ArgbEvaluator.md) | This evaluator can be used to perform type interpolation between integer values that represent ARGB colors. |
| [BidirectionalTypeConverter](BidirectionalTypeConverter.md) | Abstract base class used convert type T to another type V and back again. |
| [FloatArrayEvaluator](FloatArrayEvaluator.md) | This evaluator can be used to perform type interpolation between`float[]`values. |
| --- | --- |
| [FloatEvaluator](FloatEvaluator.md) | This evaluator can be used to perform type interpolation between`float`values. |
| [IntArrayEvaluator](IntArrayEvaluator.md) | This evaluator can be used to perform type interpolation between`int[]`values. |
| [IntEvaluator](IntEvaluator.md) | This evaluator can be used to perform type interpolation between`int`values. |
| --- | --- |
| [Keyframe](Keyframe.md) | This class holds a time/value pair for an animation. |
| [LayoutTransition](LayoutTransition.md) | This class enables automatic animations on layout changes in ViewGroup objects. |
| [ObjectAnimator](ObjectAnimator.md) | This subclass of [ValueAnimator](ValueAnimator.md) provides support for animating properties on target objects. |
| --- | --- |
| [PointFEvaluator](PointFEvaluator.md) | This evaluator can be used to perform type interpolation between`PointF`values. |
| [PropertyValuesHolder](PropertyValuesHolder.md) | This class holds information about a property and the values that that property should take on during an animation. |
| [RectEvaluator](RectEvaluator.md) | This evaluator can be used to perform type interpolation between`Rect`values. |
| --- | --- |
| [StateListAnimator](StateListAnimator.md) | Lets you define a number of Animators that will run on the attached View depending on the View's drawable state. |
| [TimeAnimator](TimeAnimator.md) | This class provides a simple callback mechanism to listeners that is synchronized with all other animators in the system. |
| [TypeConverter](TypeConverter.md) | Abstract base class used convert type T to another type V. |
| --- | --- |
| [ValueAnimator](ValueAnimator.md) | This class provides a simple timing engine for running animations which calculate animated values and set them on target objects. |
