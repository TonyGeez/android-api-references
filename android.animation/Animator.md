# Animator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Animator

Kotlin| [Java](../android/animation/Animator.md) 
| --- | --- |

```
abstract class Animator : Cloneable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.animation.Animator](../android/animation/Animator.md) |

| Known Direct Subclasses [AnimatorSet](../android/animation/AnimatorSet.md), [ValueAnimator](../android/animation/ValueAnimator.md) |-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------| | [AnimatorSet](../android/animation/AnimatorSet.md) | This class plays a set of [Animator](../android/animation/Animator.md) objects in the specified order. | | [ValueAnimator](../android/animation/ValueAnimator.md) | This class provides a simple timing engine for running animations which calculate animated values and set them on target objects. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ObjectAnimator](../android/animation/ObjectAnimator.md), [TimeAnimator](../android/animation/TimeAnimator.md) |---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ObjectAnimator](../android/animation/ObjectAnimator.md) | This subclass of [ValueAnimator](../android/animation/ValueAnimator.md) provides support for animating properties on target objects. | | [TimeAnimator](../android/animation/TimeAnimator.md) | This class provides a simple callback mechanism to listeners that is synchronized with all other animators in the system. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This is the superclass for classes which provide basic support for animations which can be started, ended, and have`AnimatorListeners`added to them.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [AnimatorListener](../android/animation/Animator.AnimatorListener.md) An animation listener receives notifications from an animation. |
| abstract | [AnimatorPauseListener](../android/animation/Animator.AnimatorPauseListener.md) A pause listener receives notifications from an animation when the animation is [paused](../android/animation/Animator.md))or [resumed](../android/animation/Animator.md)). |

| Constants ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [DURATION_INFINITE](../android/animation/Animator.md) The value used to indicate infinite duration (e.g. when Animators repeat infinitely). |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------|---|
| [Animator](../android/animation/Animator.md))`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addListener](../android/animation/Animator.md))`(`listener:` ` [Animator.AnimatorListener](../android/animation/Animator.AnimatorListener.md)!`)` Adds a listener to the set of listeners that are sent events through the life of an animation, such as start, repeat, and end. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addPauseListener](../android/animation/Animator.md))`(`listener:` ` [Animator.AnimatorPauseListener](../android/animation/Animator.AnimatorPauseListener.md)!`)` Adds a pause listener to this animator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](../android/animation/Animator.md))`()` Cancels the animation. |
| --- | --- |
| open [Animator](../android/animation/Animator.md) | [clone](../android/animation/Animator.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [end](../android/animation/Animator.md))`()` Ends the animation. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDuration](../android/animation/Animator.md))`()` Gets the duration of the animation. |
| --- | --- |
| open [TimeInterpolator](../android/animation/TimeInterpolator.md)! | [getInterpolator](../android/animation/Animator.md))`()` Returns the timing interpolator that this animation uses. |
| open [ArrayList](../java/util/ArrayList.md)\< [Animator.AnimatorListener](../android/animation/Animator.AnimatorListener.md)!\>! | [getListeners](../android/animation/Animator.md))`()` Gets the set of [android.animation.Animator.AnimatorListener](../android/animation/Animator.AnimatorListener.md) objects that are currently listening for events on this`Animator`object. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartDelay](../android/animation/Animator.md))`()` The amount of time, in milliseconds, to delay processing the animation after [start()](../android/animation/Animator.md))is called. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTotalDuration](../android/animation/Animator.md))`()` Gets the total duration of the animation, accounting for animation sequences, start delay, and repeating. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPaused](../android/animation/Animator.md))`()` Returns whether this animator is currently in a paused state. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRunning](../android/animation/Animator.md))`()` Returns whether this Animator is currently running (having been started and gone past any initial startDelay period and not yet ended). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStarted](../android/animation/Animator.md))`()` Returns whether this Animator has been started and not yet ended. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [pause](../android/animation/Animator.md))`()` Pauses a running animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeAllListeners](../android/animation/Animator.md))`()` Removes all [listeners](../android/animation/Animator.md))and [pauseListeners](../android/animation/Animator.md))from this object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeListener](../android/animation/Animator.md))`(`listener:` ` [Animator.AnimatorListener](../android/animation/Animator.AnimatorListener.md)!`)` Removes a listener from the set listening to this animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removePauseListener](../android/animation/Animator.md))`(`listener:` ` [Animator.AnimatorPauseListener](../android/animation/Animator.AnimatorPauseListener.md)!`)` Removes a pause listener from the set listening to this animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resume](../android/animation/Animator.md))`()` Resumes a paused animation, causing the animator to pick up where it left off when it was paused. |
| --- | --- |
| abstract [Animator](../android/animation/Animator.md)! | [setDuration](../android/animation/Animator.md))`(`duration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the duration of the animation. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInterpolator](../android/animation/Animator.md))`(`value:` ` [TimeInterpolator](../android/animation/TimeInterpolator.md)!`)` The time interpolator used in calculating the elapsed fraction of the animation. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStartDelay](../android/animation/Animator.md))`(`startDelay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` The amount of time, in milliseconds, to delay processing the animation after [start()](../android/animation/Animator.md))is called. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTarget](../android/animation/Animator.md))`(`target:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Sets the target object whose property will be animated by this animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setupEndValues](../android/animation/Animator.md))`()` This method tells the object to use appropriate information to extract ending values for the animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setupStartValues](../android/animation/Animator.md))`()` This method tells the object to use appropriate information to extract starting values for the animation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](../android/animation/Animator.md))`()` Starts this animation. |

## Constants

### DURATION_INFINITE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DURATION_INFINITE: Long
```

The value used to indicate infinite duration (e.g. when Animators repeat infinitely). 

 Value: -1L

## Public constructors

### Animator

```
Animator()
```

## Public methods

### addListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addListener(listener: Animator.AnimatorListener!): Unit
```

Adds a listener to the set of listeners that are sent events through the life of an animation, such as start, repeat, and end.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [Animator.AnimatorListener](../android/animation/Animator.AnimatorListener.md)!:the listener to be added to the current set of listeners for this animation. |

### addPauseListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addPauseListener(listener: Animator.AnimatorPauseListener!): Unit
```

Adds a pause listener to this animator.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [Animator.AnimatorPauseListener](../android/animation/Animator.AnimatorPauseListener.md)!:the listener to be added to the current set of pause listeners for this animation. |

### cancel

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun cancel(): Unit
```

Cancels the animation. Unlike [end()](../android/animation/Animator.md)),`cancel()`causes the animation to stop in its tracks, sending an [android.animation.Animator.AnimatorListener#onAnimationCancel(Animator)](../android/animation/Animator.AnimatorListener.md))to its listeners, followed by an [android.animation.Animator.AnimatorListener#onAnimationEnd(Animator)](../android/animation/Animator.AnimatorListener.md))message.

This method must be called on the thread that is running the animation. 

### clone

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Animator
```

| Return ||
|----------------------------------------------------------------------------------------|---------------------------|
| [Animator](../android/animation/Animator.md) | a clone of this instance. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### end

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun end(): Unit
```

Ends the animation. This causes the animation to assign the end value of the property being animated, then calling the [android.animation.Animator.AnimatorListener#onAnimationEnd(Animator)](../android/animation/Animator.AnimatorListener.md))method on its listeners.

This method must be called on the thread that is running the animation. 

### getDuration

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDuration(): Long
```

Gets the duration of the animation.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The length of the animation, in milliseconds. |

### getInterpolator

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInterpolator(): TimeInterpolator!
```

Returns the timing interpolator that this animation uses.

| Return ||
|--------------------------------------------------------------------------------------------------------|---------------------------------------------|
| [TimeInterpolator](../android/animation/TimeInterpolator.md)! | The timing interpolator for this animation. |

### getListeners

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getListeners(): ArrayList<Animator.AnimatorListener!>!
```

Gets the set of [android.animation.Animator.AnimatorListener](../android/animation/Animator.AnimatorListener.md) objects that are currently listening for events on this`Animator`object.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| [ArrayList](../java/util/ArrayList.md)< [Animator.AnimatorListener](../android/animation/Animator.AnimatorListener.md)!>! | ArrayList The set of listeners. |

### getStartDelay

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getStartDelay(): Long
```

The amount of time, in milliseconds, to delay processing the animation after [start()](../android/animation/Animator.md))is called.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the number of milliseconds to delay running the animation |

### getTotalDuration

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTotalDuration(): Long
```

Gets the total duration of the animation, accounting for animation sequences, start delay, and repeating. Return [DURATION_INFINITE](../android/animation/Animator.md) if the duration is infinite.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Total time an animation takes to finish, starting from the time [start()](../android/animation/Animator.md))is called. [DURATION_INFINITE](../android/animation/Animator.md) will be returned if the animation or any child animation repeats infinite times. |

### isPaused

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isPaused(): Boolean
```

Returns whether this animator is currently in a paused state.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the animator is currently paused, false otherwise. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/animation/Animator#pause()>
- <https://developer.android.com/reference/kotlin/android/animation/Animator#resume()> 

### isRunning

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isRunning(): Boolean
```

Returns whether this Animator is currently running (having been started and gone past any initial startDelay period and not yet ended).

| Return ||
|------------------------------------------------------------------------------------|----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the Animator is running. |

### isStarted

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isStarted(): Boolean
```

Returns whether this Animator has been started and not yet ended. For reusable Animators (which most Animators are, apart from the one-shot animator produced by [createCircularReveal()](../android/view/ViewAnimationUtils.md))), this state is a superset of [isRunning()](../android/animation/Animator.md)), because an Animator with a nonzero [startDelay](../android/animation/Animator.md))will return true for [isStarted()](../android/animation/Animator.md))during the delay phase, whereas [isRunning()](../android/animation/Animator.md))will return true only after the delay phase is complete. Non-reusable animators will always return true after they have been started, because they cannot return to a non-started state.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the Animator has been started and not yet ended. |

### pause

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pause(): Unit
```

Pauses a running animation. This method should only be called on the same thread on which the animation was started. If the animation has not yet been [started](../android/animation/Animator.md))or has since ended, then the call is ignored. Paused animations can be resumed by calling [resume()](../android/animation/Animator.md)). 
**See Also**

- <https://developer.android.com/reference/kotlin/android/animation/Animator#resume()>
- <https://developer.android.com/reference/kotlin/android/animation/Animator#isPaused()>
- [android.animation.Animator.AnimatorPauseListener](../android/animation/Animator.AnimatorPauseListener.md) 

### removeAllListeners

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeAllListeners(): Unit
```

Removes all [listeners](../android/animation/Animator.md))and [pauseListeners](../android/animation/Animator.md))from this object. 

### removeListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeListener(listener: Animator.AnimatorListener!): Unit
```

Removes a listener from the set listening to this animation.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [Animator.AnimatorListener](../android/animation/Animator.AnimatorListener.md)!:the listener to be removed from the current set of listeners for this animation. |

### removePauseListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removePauseListener(listener: Animator.AnimatorPauseListener!): Unit
```

Removes a pause listener from the set listening to this animation.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [Animator.AnimatorPauseListener](../android/animation/Animator.AnimatorPauseListener.md)!:the listener to be removed from the current set of pause listeners for this animation. |

### resume

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun resume(): Unit
```

Resumes a paused animation, causing the animator to pick up where it left off when it was paused. This method should only be called on the same thread on which the animation was started. Calls to resume() on an animator that is not currently paused will be ignored. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/animation/Animator#pause()>
- <https://developer.android.com/reference/kotlin/android/animation/Animator#isPaused()>
- [android.animation.Animator.AnimatorPauseListener](../android/animation/Animator.AnimatorPauseListener.md) 

### setDuration

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDuration(duration: Long): Animator!
```

Sets the duration of the animation.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------|
| `duration` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The length of the animation, in milliseconds. |

### setInterpolator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setInterpolator(value: TimeInterpolator!): Unit
```

The time interpolator used in calculating the elapsed fraction of the animation. The interpolator determines whether the animation runs with linear or non-linear motion, such as acceleration and deceleration. The default value is [android.view.animation.AccelerateDecelerateInterpolator](../android/view/animation/AccelerateDecelerateInterpolator.md).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [TimeInterpolator](../android/animation/TimeInterpolator.md)!:the interpolator to be used by this animation |

### setStartDelay

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setStartDelay(startDelay: Long): Unit
```

The amount of time, in milliseconds, to delay processing the animation after [start()](../android/animation/Animator.md))is called.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| `startDelay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The amount of the delay, in milliseconds |

### setTarget

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTarget(target: Any?): Unit
```

Sets the target object whose property will be animated by this animation. Not all subclasses operate on target objects (for example, [ValueAnimator](../android/animation/ValueAnimator.md), but this method is on the superclass for the convenience of dealing generically with those subclasses that do handle targets.

**Note:**The target is stored as a weak reference internally to avoid leaking resources by having animators directly reference old targets. Therefore, you should ensure that animator targets always have a hard reference elsewhere.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------|
| `target` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:The object being animated This value may be`null`. |

### setupEndValues

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setupEndValues(): Unit
```

This method tells the object to use appropriate information to extract ending values for the animation. For example, a AnimatorSet object will pass this call to its child objects to tell them to set up the values. A ObjectAnimator object will use the information it has about its target object and PropertyValuesHolder objects to get the start values for its properties. A ValueAnimator object will ignore the request since it does not have enough information (such as a target object) to gather these values. 

### setupStartValues

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setupStartValues(): Unit
```

This method tells the object to use appropriate information to extract starting values for the animation. For example, a AnimatorSet object will pass this call to its child objects to tell them to set up the values. A ObjectAnimator object will use the information it has about its target object and PropertyValuesHolder objects to get the start values for its properties. A ValueAnimator object will ignore the request since it does not have enough information (such as a target object) to gather these values. 

### start

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun start(): Unit
```

Starts this animation. If the animation has a nonzero startDelay, the animation will start running after that delay elapses. A non-delayed animation will have its initial value(s) set immediately, followed by calls to [AnimatorListener.onAnimationStart(Animator)](../android/animation/Animator.AnimatorListener.md))for any listeners of this animator.

The animation started by calling this method will be run on the thread that called this method. This thread should have a Looper on it (a runtime exception will be thrown if this is not the case). Also, if the animation will animate properties of objects in the view hierarchy, then the calling thread should be the UI thread for that view hierarchy.
