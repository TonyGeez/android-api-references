# Animator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Animator

Kotlin| [Java](https://developer.android.com/reference/android/animation/Animator "View this page in Java") 
| --- | --- |

```
abstract class Animator : Cloneable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.animation.Animator](https://developer.android.com/reference/kotlin/android/animation/Animator#) |

| Known Direct Subclasses [AnimatorSet](https://developer.android.com/reference/kotlin/android/animation/AnimatorSet), [ValueAnimator](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator) |-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------| | [AnimatorSet](https://developer.android.com/reference/kotlin/android/animation/AnimatorSet) | This class plays a set of [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator#) objects in the specified order. | | [ValueAnimator](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator) | This class provides a simple timing engine for running animations which calculate animated values and set them on target objects. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator), [TimeAnimator](https://developer.android.com/reference/kotlin/android/animation/TimeAnimator) |---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator) | This subclass of [ValueAnimator](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator) provides support for animating properties on target objects. | | [TimeAnimator](https://developer.android.com/reference/kotlin/android/animation/TimeAnimator) | This class provides a simple callback mechanism to listeners that is synchronized with all other animators in the system. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This is the superclass for classes which provide basic support for animations which can be started, ended, and have`AnimatorListeners`added to them.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [AnimatorListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener) An animation listener receives notifications from an animation. |
| abstract | [AnimatorPauseListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorPauseListener) A pause listener receives notifications from an animation when the animation is [paused](https://developer.android.com/reference/kotlin/android/animation/Animator#pause())or [resumed](https://developer.android.com/reference/kotlin/android/animation/Animator#resume()). |

| Constants ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [DURATION_INFINITE](https://developer.android.com/reference/kotlin/android/animation/Animator#DURATION_INFINITE:kotlin.Long) The value used to indicate infinite duration (e.g. when Animators repeat infinitely). |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------|---|
| [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator#Animator())`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addListener](https://developer.android.com/reference/kotlin/android/animation/Animator#addListener(android.animation.Animator.AnimatorListener))`(`listener:` ` [Animator.AnimatorListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener)!`)` Adds a listener to the set of listeners that are sent events through the life of an animation, such as start, repeat, and end. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addPauseListener](https://developer.android.com/reference/kotlin/android/animation/Animator#addPauseListener(android.animation.Animator.AnimatorPauseListener))`(`listener:` ` [Animator.AnimatorPauseListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorPauseListener)!`)` Adds a pause listener to this animator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](https://developer.android.com/reference/kotlin/android/animation/Animator#cancel())`()` Cancels the animation. |
| --- | --- |
| open [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator#) | [clone](https://developer.android.com/reference/kotlin/android/animation/Animator#clone())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [end](https://developer.android.com/reference/kotlin/android/animation/Animator#end())`()` Ends the animation. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDuration](https://developer.android.com/reference/kotlin/android/animation/Animator#getDuration())`()` Gets the duration of the animation. |
| --- | --- |
| open [TimeInterpolator](https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator)! | [getInterpolator](https://developer.android.com/reference/kotlin/android/animation/Animator#getInterpolator())`()` Returns the timing interpolator that this animation uses. |
| open [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [Animator.AnimatorListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener)!\>! | [getListeners](https://developer.android.com/reference/kotlin/android/animation/Animator#getListeners())`()` Gets the set of [android.animation.Animator.AnimatorListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener) objects that are currently listening for events on this`Animator`object. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartDelay](https://developer.android.com/reference/kotlin/android/animation/Animator#getStartDelay())`()` The amount of time, in milliseconds, to delay processing the animation after [start()](https://developer.android.com/reference/kotlin/android/animation/Animator#start())is called. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTotalDuration](https://developer.android.com/reference/kotlin/android/animation/Animator#getTotalDuration())`()` Gets the total duration of the animation, accounting for animation sequences, start delay, and repeating. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPaused](https://developer.android.com/reference/kotlin/android/animation/Animator#isPaused())`()` Returns whether this animator is currently in a paused state. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRunning](https://developer.android.com/reference/kotlin/android/animation/Animator#isRunning())`()` Returns whether this Animator is currently running (having been started and gone past any initial startDelay period and not yet ended). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStarted](https://developer.android.com/reference/kotlin/android/animation/Animator#isStarted())`()` Returns whether this Animator has been started and not yet ended. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [pause](https://developer.android.com/reference/kotlin/android/animation/Animator#pause())`()` Pauses a running animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeAllListeners](https://developer.android.com/reference/kotlin/android/animation/Animator#removeAllListeners())`()` Removes all [listeners](https://developer.android.com/reference/kotlin/android/animation/Animator#addListener(android.animation.Animator.AnimatorListener))and [pauseListeners](https://developer.android.com/reference/kotlin/android/animation/Animator#addPauseListener(android.animation.Animator.AnimatorPauseListener))from this object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeListener](https://developer.android.com/reference/kotlin/android/animation/Animator#removeListener(android.animation.Animator.AnimatorListener))`(`listener:` ` [Animator.AnimatorListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener)!`)` Removes a listener from the set listening to this animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removePauseListener](https://developer.android.com/reference/kotlin/android/animation/Animator#removePauseListener(android.animation.Animator.AnimatorPauseListener))`(`listener:` ` [Animator.AnimatorPauseListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorPauseListener)!`)` Removes a pause listener from the set listening to this animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resume](https://developer.android.com/reference/kotlin/android/animation/Animator#resume())`()` Resumes a paused animation, causing the animator to pick up where it left off when it was paused. |
| --- | --- |
| abstract [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator#)! | [setDuration](https://developer.android.com/reference/kotlin/android/animation/Animator#setDuration(kotlin.Long))`(`duration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the duration of the animation. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInterpolator](https://developer.android.com/reference/kotlin/android/animation/Animator#setInterpolator(android.animation.TimeInterpolator))`(`value:` ` [TimeInterpolator](https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator)!`)` The time interpolator used in calculating the elapsed fraction of the animation. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStartDelay](https://developer.android.com/reference/kotlin/android/animation/Animator#setStartDelay(kotlin.Long))`(`startDelay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` The amount of time, in milliseconds, to delay processing the animation after [start()](https://developer.android.com/reference/kotlin/android/animation/Animator#start())is called. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTarget](https://developer.android.com/reference/kotlin/android/animation/Animator#setTarget(kotlin.Any))`(`target:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Sets the target object whose property will be animated by this animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setupEndValues](https://developer.android.com/reference/kotlin/android/animation/Animator#setupEndValues())`()` This method tells the object to use appropriate information to extract ending values for the animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setupStartValues](https://developer.android.com/reference/kotlin/android/animation/Animator#setupStartValues())`()` This method tells the object to use appropriate information to extract starting values for the animation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](https://developer.android.com/reference/kotlin/android/animation/Animator#start())`()` Starts this animation. |

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
| `listener` | [Animator.AnimatorListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener)!:the listener to be added to the current set of listeners for this animation. |

### addPauseListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addPauseListener(listener: Animator.AnimatorPauseListener!): Unit
```

Adds a pause listener to this animator.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [Animator.AnimatorPauseListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorPauseListener)!:the listener to be added to the current set of pause listeners for this animation. |

### cancel

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun cancel(): Unit
```

Cancels the animation. Unlike [end()](https://developer.android.com/reference/kotlin/android/animation/Animator#end()),`cancel()`causes the animation to stop in its tracks, sending an [android.animation.Animator.AnimatorListener#onAnimationCancel(Animator)](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener#onAnimationCancel(android.animation.Animator))to its listeners, followed by an [android.animation.Animator.AnimatorListener#onAnimationEnd(Animator)](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener#onAnimationEnd(android.animation.Animator))message.

This method must be called on the thread that is running the animation. 

### clone

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Animator
```

| Return ||
|----------------------------------------------------------------------------------------|---------------------------|
| [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator#) | a clone of this instance. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### end

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun end(): Unit
```

Ends the animation. This causes the animation to assign the end value of the property being animated, then calling the [android.animation.Animator.AnimatorListener#onAnimationEnd(Animator)](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener#onAnimationEnd(android.animation.Animator))method on its listeners.

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
| [TimeInterpolator](https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator)! | The timing interpolator for this animation. |

### getListeners

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getListeners(): ArrayList<Animator.AnimatorListener!>!
```

Gets the set of [android.animation.Animator.AnimatorListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener) objects that are currently listening for events on this`Animator`object.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)< [Animator.AnimatorListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener)!>! | ArrayList The set of listeners. |

### getStartDelay

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getStartDelay(): Long
```

The amount of time, in milliseconds, to delay processing the animation after [start()](https://developer.android.com/reference/kotlin/android/animation/Animator#start())is called.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the number of milliseconds to delay running the animation |

### getTotalDuration

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTotalDuration(): Long
```

Gets the total duration of the animation, accounting for animation sequences, start delay, and repeating. Return [DURATION_INFINITE](https://developer.android.com/reference/kotlin/android/animation/Animator#DURATION_INFINITE:kotlin.Long) if the duration is infinite.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Total time an animation takes to finish, starting from the time [start()](https://developer.android.com/reference/kotlin/android/animation/Animator#start())is called. [DURATION_INFINITE](https://developer.android.com/reference/kotlin/android/animation/Animator#DURATION_INFINITE:kotlin.Long) will be returned if the animation or any child animation repeats infinite times. |

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

Returns whether this Animator has been started and not yet ended. For reusable Animators (which most Animators are, apart from the one-shot animator produced by [createCircularReveal()](https://developer.android.com/reference/kotlin/android/view/ViewAnimationUtils.html#createCircularReveal(android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float))), this state is a superset of [isRunning()](https://developer.android.com/reference/kotlin/android/animation/Animator#isRunning()), because an Animator with a nonzero [startDelay](https://developer.android.com/reference/kotlin/android/animation/Animator#getStartDelay())will return true for [isStarted()](https://developer.android.com/reference/kotlin/android/animation/Animator#isStarted())during the delay phase, whereas [isRunning()](https://developer.android.com/reference/kotlin/android/animation/Animator#isRunning())will return true only after the delay phase is complete. Non-reusable animators will always return true after they have been started, because they cannot return to a non-started state.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the Animator has been started and not yet ended. |

### pause

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pause(): Unit
```

Pauses a running animation. This method should only be called on the same thread on which the animation was started. If the animation has not yet been [started](https://developer.android.com/reference/kotlin/android/animation/Animator#isStarted())or has since ended, then the call is ignored. Paused animations can be resumed by calling [resume()](https://developer.android.com/reference/kotlin/android/animation/Animator#resume()). 
**See Also**

- <https://developer.android.com/reference/kotlin/android/animation/Animator#resume()>
- <https://developer.android.com/reference/kotlin/android/animation/Animator#isPaused()>
- [android.animation.Animator.AnimatorPauseListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorPauseListener) 

### removeAllListeners

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeAllListeners(): Unit
```

Removes all [listeners](https://developer.android.com/reference/kotlin/android/animation/Animator#addListener(android.animation.Animator.AnimatorListener))and [pauseListeners](https://developer.android.com/reference/kotlin/android/animation/Animator#addPauseListener(android.animation.Animator.AnimatorPauseListener))from this object. 

### removeListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeListener(listener: Animator.AnimatorListener!): Unit
```

Removes a listener from the set listening to this animation.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [Animator.AnimatorListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener)!:the listener to be removed from the current set of listeners for this animation. |

### removePauseListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removePauseListener(listener: Animator.AnimatorPauseListener!): Unit
```

Removes a pause listener from the set listening to this animation.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [Animator.AnimatorPauseListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorPauseListener)!:the listener to be removed from the current set of pause listeners for this animation. |

### resume

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun resume(): Unit
```

Resumes a paused animation, causing the animator to pick up where it left off when it was paused. This method should only be called on the same thread on which the animation was started. Calls to resume() on an animator that is not currently paused will be ignored. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/animation/Animator#pause()>
- <https://developer.android.com/reference/kotlin/android/animation/Animator#isPaused()>
- [android.animation.Animator.AnimatorPauseListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorPauseListener) 

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

The time interpolator used in calculating the elapsed fraction of the animation. The interpolator determines whether the animation runs with linear or non-linear motion, such as acceleration and deceleration. The default value is [android.view.animation.AccelerateDecelerateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AccelerateDecelerateInterpolator.html#).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [TimeInterpolator](https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator)!:the interpolator to be used by this animation |

### setStartDelay

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setStartDelay(startDelay: Long): Unit
```

The amount of time, in milliseconds, to delay processing the animation after [start()](https://developer.android.com/reference/kotlin/android/animation/Animator#start())is called.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| `startDelay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The amount of the delay, in milliseconds |

### setTarget

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTarget(target: Any?): Unit
```

Sets the target object whose property will be animated by this animation. Not all subclasses operate on target objects (for example, [ValueAnimator](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator), but this method is on the superclass for the convenience of dealing generically with those subclasses that do handle targets.

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

Starts this animation. If the animation has a nonzero startDelay, the animation will start running after that delay elapses. A non-delayed animation will have its initial value(s) set immediately, followed by calls to [AnimatorListener.onAnimationStart(Animator)](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener#onAnimationStart(android.animation.Animator))for any listeners of this animator.

The animation started by calling this method will be run on the thread that called this method. This thread should have a Looper on it (a runtime exception will be thrown if this is not the case). Also, if the animation will animate properties of objects in the view hierarchy, then the calling thread should be the UI thread for that view hierarchy.
