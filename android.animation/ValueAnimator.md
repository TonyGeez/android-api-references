# ValueAnimator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ValueAnimator

Kotlin| [Java](../android/animation/ValueAnimator.md) 
| --- | --- |

```
open class ValueAnimator : Animator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.animation.Animator](../android/animation/Animator.md) ||
| | ↳ | [android.animation.ValueAnimator](../android/animation/ValueAnimator.md) |

| Known Direct Subclasses [ObjectAnimator](../android/animation/ObjectAnimator.md), [TimeAnimator](../android/animation/TimeAnimator.md) |---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ObjectAnimator](../android/animation/ObjectAnimator.md) | This subclass of [ValueAnimator](../android/animation/ValueAnimator.md) provides support for animating properties on target objects. | | [TimeAnimator](../android/animation/TimeAnimator.md) | This class provides a simple callback mechanism to listeners that is synchronized with all other animators in the system. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This class provides a simple timing engine for running animations which calculate animated values and set them on target objects.

There is a single timing pulse that all animations use. It runs in a custom handler to ensure that property changes happen on the UI thread.

By default, ValueAnimator uses non-linear time interpolation, via the [AccelerateDecelerateInterpolator](../android/view/animation/AccelerateDecelerateInterpolator.md) class, which accelerates into and decelerates out of an animation. This behavior can be changed by calling [ValueAnimator.setInterpolator(TimeInterpolator)](../android/animation/ValueAnimator.md)).

Animators can be created from either code or resource files. Here is an example of a ValueAnimator resource file:

Starting from API 23, it is also possible to use a combination of [PropertyValuesHolder](../android/animation/PropertyValuesHolder.md) and [Keyframe](../android/animation/Keyframe.md) resource tags to create a multi-step animation. Note that you can specify explicit fractional values (from 0 to 1) for each keyframe to determine when, in the overall duration, the animation should arrive at that value. Alternatively, you can leave the fractions off and the keyframes will be equally distributed within the total duration:
|
| ### Developer Guides
|
| For more information about animating with`ValueAnimator`, read the [Property Animation](https://developer.android.com/guide/topics/graphics/prop-animation.html#value-animator) developer guide.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [AnimatorUpdateListener](../android/animation/ValueAnimator.AnimatorUpdateListener.md) Implementors of this interface can add themselves as update listeners to an`ValueAnimator`instance to receive callbacks on every animation frame, after the current frame's values have been calculated for that`ValueAnimator`. |
| abstract | [DurationScaleChangeListener](../android/animation/ValueAnimator.DurationScaleChangeListener.md) Listener interface for the system-wide scaling factor for Animator-based animations. |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INFINITE](../android/animation/ValueAnimator.md) This value used used with the [setRepeatCount(int)](../android/animation/ValueAnimator.md))property to repeat the animation indefinitely. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESTART](../android/animation/ValueAnimator.md) When the animation reaches the end and`repeatCount`is INFINITE or a positive value, the animation restarts from the beginning. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REVERSE](../android/animation/ValueAnimator.md) When the animation reaches the end and`repeatCount`is INFINITE or a positive value, the animation reverses direction on every iteration. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Animator](../android/animation/Animator.md) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [DURATION_INFINITE](../android/animation/Animator.md) <br /> The value used to indicate infinite duration (e.g. when Animators repeat infinitely). <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ValueAnimator](../android/animation/ValueAnimator.md))`()` Creates a new ValueAnimator object. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addUpdateListener](../android/animation/ValueAnimator.md))`(`listener:` ` [ValueAnimator.AnimatorUpdateListener](../android/animation/ValueAnimator.AnimatorUpdateListener.md)!`)` Adds a listener to the set of listeners that are sent update events through the life of an animation. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areAnimatorsEnabled](../android/animation/ValueAnimator.md))`()` Returns whether animators are currently enabled, system-wide. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](../android/animation/ValueAnimator.md))`()` <br /> |
| --- | --- |
| open [ValueAnimator](../android/animation/ValueAnimator.md) | [clone](../android/animation/ValueAnimator.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [end](../android/animation/ValueAnimator.md))`()` <br /> |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getAnimatedFraction](../android/animation/ValueAnimator.md))`()` Returns the current animation fraction, which is the elapsed/interpolated fraction used in the most recent frame update on the animation. |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAnimatedValue](../android/animation/ValueAnimator.md))`()` The most recent value calculated by this`ValueAnimator`when there is just one property being animated. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAnimatedValue](../android/animation/ValueAnimator.md))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` The most recent value calculated by this`ValueAnimator`for`propertyName`. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCurrentPlayTime](../android/animation/ValueAnimator.md))`()` Gets the current position of the animation in time, which is equal to the current time minus the time that the animation started. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDuration](../android/animation/ValueAnimator.md))`()` Gets the length of the animation. |
| openstatic [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getDurationScale](../android/animation/ValueAnimator.md))`()` Returns the system-wide scaling factor for Animator-based animations. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getFrameDelay](../android/animation/ValueAnimator.md))`()` The amount of time, in milliseconds, between each frame of the animation. |
| --- | --- |
| open [TimeInterpolator](../android/animation/TimeInterpolator.md)! | [getInterpolator](../android/animation/ValueAnimator.md))`()` Returns the timing interpolator that this ValueAnimator uses. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRepeatCount](../android/animation/ValueAnimator.md))`()` Defines how many times the animation should repeat. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRepeatMode](../android/animation/ValueAnimator.md))`()` Defines what this animation should do when it reaches the end. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartDelay](../android/animation/ValueAnimator.md))`()` The amount of time, in milliseconds, to delay starting the animation after [start()](../android/animation/ValueAnimator.md))is called. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTotalDuration](../android/animation/ValueAnimator.md))`()` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [PropertyValuesHolder](../android/animation/PropertyValuesHolder.md)!\>! | [getValues](../android/animation/ValueAnimator.md))`()` Returns the values that this ValueAnimator animates between. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRunning](../android/animation/ValueAnimator.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStarted](../android/animation/ValueAnimator.md))`()` <br /> |
| openstatic [ValueAnimator](../android/animation/ValueAnimator.md)! | [ofArgb](../android/animation/ValueAnimator.md))`(`vararg` `values:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs and returns a ValueAnimator that animates between color values. |
| --- | --- |
| openstatic [ValueAnimator](../android/animation/ValueAnimator.md)! | [ofFloat](../android/animation/ValueAnimator.md))`(`vararg` `values:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Constructs and returns a ValueAnimator that animates between float values. |
| openstatic [ValueAnimator](../android/animation/ValueAnimator.md)! | [ofInt](../android/animation/ValueAnimator.md))`(`vararg` `values:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs and returns a ValueAnimator that animates between int values. |
| openstatic [ValueAnimator](../android/animation/ValueAnimator.md)! | [ofObject](../android/animation/ValueAnimator.md))`(`evaluator:` ` [TypeEvaluator](../android/animation/TypeEvaluator.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`, `vararg` `values:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Constructs and returns a ValueAnimator that animates between Object values. |
| --- | --- |
| openstatic [ValueAnimator](../android/animation/ValueAnimator.md)! | [ofPropertyValuesHolder](../android/animation/ValueAnimator.md))`(`vararg` `values:` ` [PropertyValuesHolder](../android/animation/PropertyValuesHolder.md)!`)` Constructs and returns a ValueAnimator that animates between the values specified in the PropertyValuesHolder objects. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [pause](../android/animation/ValueAnimator.md))`()` <br /> |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerDurationScaleChangeListener](../android/animation/ValueAnimator.md))`(`listener:` ` [ValueAnimator.DurationScaleChangeListener](../android/animation/ValueAnimator.DurationScaleChangeListener.md)`)` Registers a [DurationScaleChangeListener](../android/animation/ValueAnimator.DurationScaleChangeListener.md) This listens for changes to the system-wide scaling factor for Animator-based animations. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeAllUpdateListeners](../android/animation/ValueAnimator.md))`()` Removes all listeners from the set listening to frame updates for this animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeUpdateListener](../android/animation/ValueAnimator.md))`(`listener:` ` [ValueAnimator.AnimatorUpdateListener](../android/animation/ValueAnimator.AnimatorUpdateListener.md)!`)` Removes a listener from the set listening to frame updates for this animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resume](../android/animation/ValueAnimator.md))`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reverse](../android/animation/ValueAnimator.md))`()` Plays the ValueAnimator in reverse. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCurrentFraction](../android/animation/ValueAnimator.md))`(`fraction:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the position of the animation to the specified fraction. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCurrentPlayTime](../android/animation/ValueAnimator.md))`(`playTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the position of the animation to the specified point in time. |
| --- | --- |
| open [ValueAnimator](../android/animation/ValueAnimator.md)! | [setDuration](../android/animation/ValueAnimator.md))`(`duration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the length of the animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEvaluator](../android/animation/ValueAnimator.md))`(`value:` ` [TypeEvaluator](../android/animation/TypeEvaluator.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` The type evaluator to be used when calculating the animated values of this animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFloatValues](../android/animation/ValueAnimator.md))`(`vararg` `values:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets float values that will be animated between. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFrameDelay](../android/animation/ValueAnimator.md))`(`frameDelay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` The amount of time, in milliseconds, between each frame of the animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIntValues](../android/animation/ValueAnimator.md))`(`vararg` `values:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets int values that will be animated between. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInterpolator](../android/animation/ValueAnimator.md))`(`value:` ` [TimeInterpolator](../android/animation/TimeInterpolator.md)!`)` The time interpolator used in calculating the elapsed fraction of this animation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setObjectValues](../android/animation/ValueAnimator.md))`(`vararg` `values:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Sets the values to animate between for this animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRepeatCount](../android/animation/ValueAnimator.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets how many times the animation should be repeated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRepeatMode](../android/animation/ValueAnimator.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Defines what this animation should do when it reaches the end. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStartDelay](../android/animation/ValueAnimator.md))`(`startDelay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` The amount of time, in milliseconds, to delay starting the animation after [start()](../android/animation/ValueAnimator.md))is called. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setValues](../android/animation/ValueAnimator.md))`(`vararg` `values:` ` [PropertyValuesHolder](../android/animation/PropertyValuesHolder.md)!`)` Sets the values, per property, being animated between. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](../android/animation/ValueAnimator.md))`()` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/animation/ValueAnimator.md))`()` <br /> |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [unregisterDurationScaleChangeListener](../android/animation/ValueAnimator.md))`(`listener:` ` [ValueAnimator.DurationScaleChangeListener](../android/animation/ValueAnimator.DurationScaleChangeListener.md)`)` Unregisters a DurationScaleChangeListener. |

| Inherited functions ||
|---|---|
| From class [Animator](../android/animation/Animator.md) |------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addListener](../android/animation/Animator.md))`(`listener:` ` [Animator.AnimatorListener](../android/animation/Animator.AnimatorListener.md)!`)` <br /> Adds a listener to the set of listeners that are sent events through the life of an animation, such as start, repeat, and end. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addPauseListener](../android/animation/Animator.md))`(`listener:` ` [Animator.AnimatorPauseListener](../android/animation/Animator.AnimatorPauseListener.md)!`)` <br /> Adds a pause listener to this animator. <br /> | | [ArrayList](../java/util/ArrayList.md)< [Animator.AnimatorListener](../android/animation/Animator.AnimatorListener.md)!>! | [getListeners](../android/animation/Animator.md))`()` <br /> Gets the set of [android.animation.Animator.AnimatorListener](../android/animation/Animator.AnimatorListener.md) objects that are currently listening for events on this`Animator`object. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPaused](../android/animation/Animator.md))`()` <br /> Returns whether this animator is currently in a paused state. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeAllListeners](../android/animation/Animator.md))`()` <br /> Removes all [listeners](../android/animation/Animator.md))and [pauseListeners](../android/animation/Animator.md))from this object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeListener](../android/animation/Animator.md))`(`listener:` ` [Animator.AnimatorListener](../android/animation/Animator.AnimatorListener.md)!`)` <br /> Removes a listener from the set listening to this animation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removePauseListener](../android/animation/Animator.md))`(`listener:` ` [Animator.AnimatorPauseListener](../android/animation/Animator.AnimatorPauseListener.md)!`)` <br /> Removes a pause listener from the set listening to this animation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTarget](../android/animation/Animator.md))`(`target:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Sets the target object whose property will be animated by this animation. Not all subclasses operate on target objects (for example, [ValueAnimator](../android/animation/ValueAnimator.md), but this method is on the superclass for the convenience of dealing generically with those subclasses that do handle targets. **Note:**The target is stored as a weak reference internally to avoid leaking resources by having animators directly reference old targets. Therefore, you should ensure that animator targets always have a hard reference elsewhere. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setupEndValues](../android/animation/Animator.md))`()` <br /> This method tells the object to use appropriate information to extract ending values for the animation. For example, a AnimatorSet object will pass this call to its child objects to tell them to set up the values. A ObjectAnimator object will use the information it has about its target object and PropertyValuesHolder objects to get the start values for its properties. A ValueAnimator object will ignore the request since it does not have enough information (such as a target object) to gather these values. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setupStartValues](../android/animation/Animator.md))`()` <br /> This method tells the object to use appropriate information to extract starting values for the animation. For example, a AnimatorSet object will pass this call to its child objects to tell them to set up the values. A ObjectAnimator object will use the information it has about its target object and PropertyValuesHolder objects to get the start values for its properties. A ValueAnimator object will ignore the request since it does not have enough information (such as a target object) to gather these values. <br /> | ||

## Constants

### INFINITE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INFINITE: Int
```

This value used used with the [setRepeatCount(int)](../android/animation/ValueAnimator.md))property to repeat the animation indefinitely. 

 Value: -1

### RESTART

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESTART: Int
```

When the animation reaches the end and`repeatCount`is INFINITE or a positive value, the animation restarts from the beginning. 

 Value: 1

### REVERSE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REVERSE: Int
```

When the animation reaches the end and`repeatCount`is INFINITE or a positive value, the animation reverses direction on every iteration. 

 Value: 2

## Public constructors

### ValueAnimator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ValueAnimator()
```

Creates a new ValueAnimator object. This default constructor is primarily for use internally; the factory methods which take parameters are more generally useful.

## Public methods

### addUpdateListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addUpdateListener(listener: ValueAnimator.AnimatorUpdateListener!): Unit
```

Adds a listener to the set of listeners that are sent update events through the life of an animation. This method is called on all listeners for every frame of the animation, after the values for the animation have been calculated.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [ValueAnimator.AnimatorUpdateListener](../android/animation/ValueAnimator.AnimatorUpdateListener.md)!:the listener to be added to the current set of listeners for this animation. |

### areAnimatorsEnabled

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun areAnimatorsEnabled(): Boolean
```

Returns whether animators are currently enabled, system-wide. By default, all animators are enabled. This can change if either the user sets a Developer Option to set the animator duration scale to 0 or by Battery Savery mode being enabled (which disables all animations).

Developers should not typically need to call this method, but should an app wish to show a different experience when animators are disabled, this return value can be used as a decider of which experience to offer.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean Whether animators are currently enabled. The default value is`true`. |

### cancel

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun cancel(): Unit
```  

### clone

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): ValueAnimator
```

| Return ||
|--------------------------------------------------------------------------------------------------|---------------------------|
| [ValueAnimator](../android/animation/ValueAnimator.md) | a clone of this instance. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### end

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun end(): Unit
```  

### getAnimatedFraction

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAnimatedFraction(): Float
```

Returns the current animation fraction, which is the elapsed/interpolated fraction used in the most recent frame update on the animation.

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | Elapsed/interpolated fraction of the animation. |

### getAnimatedValue

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAnimatedValue(): Any!
```

The most recent value calculated by this`ValueAnimator`when there is just one property being animated. This value is only sensible while the animation is running. The main purpose for this read-only property is to retrieve the value from the`ValueAnimator`during a call to [AnimatorUpdateListener.onAnimationUpdate(ValueAnimator)](../android/animation/ValueAnimator.AnimatorUpdateListener.md)), which is called during each animation frame, immediately after the value is calculated.

| Return ||
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | animatedValue The value most recently calculated by this`ValueAnimator`for the single property being animated. If there are several properties being animated (specified by several PropertyValuesHolder objects in the constructor), this function returns the animated value for the first of those objects. |

### getAnimatedValue

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAnimatedValue(propertyName: String!): Any!
```

The most recent value calculated by this`ValueAnimator`for`propertyName`. The main purpose for this read-only property is to retrieve the value from the`ValueAnimator`during a call to [AnimatorUpdateListener.onAnimationUpdate(ValueAnimator)](../android/animation/ValueAnimator.AnimatorUpdateListener.md)), which is called during each animation frame, immediately after the value is calculated.

| Return ||
|-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | animatedValue The value most recently calculated for the named property by this`ValueAnimator`. |

### getCurrentPlayTime

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurrentPlayTime(): Long
```

Gets the current position of the animation in time, which is equal to the current time minus the time that the animation started. An animation that is not yet started will return a value of zero, unless the animation has has its play time set via [setCurrentPlayTime(long)](../android/animation/ValueAnimator.md))or [setCurrentFraction(float)](../android/animation/ValueAnimator.md)), in which case it will return the time that was set.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The current position in time of the animation. |

### getDuration

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDuration(): Long
```

Gets the length of the animation. The default duration is 300 milliseconds.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The length of the animation, in milliseconds. |

### getDurationScale

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDurationScale(): Float
```

Returns the system-wide scaling factor for Animator-based animations. This affects both the start delay and duration of all such animations. Setting to 0 will cause animations to end immediately. The default value is 1.0f.

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the duration scale. Value is 0.0f or greater |

### getFrameDelay

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getFrameDelay(): Long
```

The amount of time, in milliseconds, between each frame of the animation. This is a requested time that the animation will attempt to honor, but the actual delay between frames may be different, depending on system load and capabilities. This is a static function because the same delay will be applied to all animations, since they are all run off of a single timing loop. The frame delay may be ignored when the animation system uses an external timing source, such as the display refresh rate (vsync), to govern animations. Note that this method should be called from the same thread that [start()](../android/animation/ValueAnimator.md))is called in order to check the frame delay for that animation. A runtime exception will be thrown if the calling thread does not have a Looper.

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the requested time between frames, in milliseconds |

### getInterpolator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInterpolator(): TimeInterpolator!
```

Returns the timing interpolator that this ValueAnimator uses.

| Return ||
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| [TimeInterpolator](../android/animation/TimeInterpolator.md)! | The timing interpolator for this ValueAnimator. |

### getRepeatCount

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRepeatCount(): Int
```

Defines how many times the animation should repeat. The default value is 0.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of times the animation should repeat, or [INFINITE](../android/animation/ValueAnimator.md) |

### getRepeatMode

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRepeatMode(): Int
```

Defines what this animation should do when it reaches the end.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | either one of [REVERSE](../android/animation/ValueAnimator.md) or [RESTART](../android/animation/ValueAnimator.md) Value is [android.animation.ValueAnimator#RESTART](../android/animation/ValueAnimator.md), or [android.animation.ValueAnimator#REVERSE](../android/animation/ValueAnimator.md) |

### getStartDelay

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStartDelay(): Long
```

The amount of time, in milliseconds, to delay starting the animation after [start()](../android/animation/ValueAnimator.md))is called.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the number of milliseconds to delay running the animation |

### getTotalDuration

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTotalDuration(): Long
```

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Total time an animation takes to finish, starting from the time [start()](../android/animation/Animator.md))is called. [DURATION_INFINITE](../android/animation/Animator.md) will be returned if the animation or any child animation repeats infinite times. |

### getValues

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValues(): Array<PropertyValuesHolder!>!
```

Returns the values that this ValueAnimator animates between. These values are stored in PropertyValuesHolder objects, even if the ValueAnimator was created with a simple list of value objects instead.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [PropertyValuesHolder](../android/animation/PropertyValuesHolder.md)!>! | PropertyValuesHolder\[\] An array of PropertyValuesHolder objects which hold the values, per property, that define the animation. |

### isRunning

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isRunning(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the Animator is running. |

### isStarted

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isStarted(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the Animator has been started and not yet ended. |

### ofArgb

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ofArgb(vararg values: Int): ValueAnimator!
```

Constructs and returns a ValueAnimator that animates between color values. A single value implies that that value is the one being animated to. However, this is not typically useful in a ValueAnimator object because there is no way for the object to determine the starting value for the animation (unlike ObjectAnimator, which can derive that value from the target object and property being animated). Therefore, there should typically be two or more values.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `values` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A set of values that the animation will animate between over time. |

| Return ||
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [ValueAnimator](../android/animation/ValueAnimator.md)! | A ValueAnimator object that is set up to animate between the given values. |

### ofFloat

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ofFloat(vararg values: Float): ValueAnimator!
```

Constructs and returns a ValueAnimator that animates between float values. A single value implies that that value is the one being animated to. However, this is not typically useful in a ValueAnimator object because there is no way for the object to determine the starting value for the animation (unlike ObjectAnimator, which can derive that value from the target object and property being animated). Therefore, there should typically be two or more values.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `values` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):A set of values that the animation will animate between over time. |

| Return ||
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [ValueAnimator](../android/animation/ValueAnimator.md)! | A ValueAnimator object that is set up to animate between the given values. |

### ofInt

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ofInt(vararg values: Int): ValueAnimator!
```

Constructs and returns a ValueAnimator that animates between int values. A single value implies that that value is the one being animated to. However, this is not typically useful in a ValueAnimator object because there is no way for the object to determine the starting value for the animation (unlike ObjectAnimator, which can derive that value from the target object and property being animated). Therefore, there should typically be two or more values.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `values` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A set of values that the animation will animate between over time. |

| Return ||
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [ValueAnimator](../android/animation/ValueAnimator.md)! | A ValueAnimator object that is set up to animate between the given values. |

### ofObject

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ofObject(
    evaluator: TypeEvaluator<Any!>!, 
    vararg values: Any!
): ValueAnimator!
```

Constructs and returns a ValueAnimator that animates between Object values. A single value implies that that value is the one being animated to. However, this is not typically useful in a ValueAnimator object because there is no way for the object to determine the starting value for the animation (unlike ObjectAnimator, which can derive that value from the target object and property being animated). Therefore, there should typically be two or more values.

**Note:**The Object values are stored as references to the original objects, which means that changes to those objects after this method is called will affect the values on the animator. If the objects will be mutated externally after this method is called, callers should pass a copy of those objects instead.

Since ValueAnimator does not know how to animate between arbitrary Objects, this factory method also takes a TypeEvaluator object that the ValueAnimator will use to perform that interpolation.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `evaluator` | [TypeEvaluator](../android/animation/TypeEvaluator.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:A TypeEvaluator that will be called on each animation frame to provide the ncessry interpolation between the Object values to derive the animated value. |
| `values` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:A set of values that the animation will animate between over time. |

| Return ||
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [ValueAnimator](../android/animation/ValueAnimator.md)! | A ValueAnimator object that is set up to animate between the given values. |

### ofPropertyValuesHolder

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ofPropertyValuesHolder(vararg values: PropertyValuesHolder!): ValueAnimator!
```

Constructs and returns a ValueAnimator that animates between the values specified in the PropertyValuesHolder objects.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `values` | [PropertyValuesHolder](../android/animation/PropertyValuesHolder.md)!:A set of PropertyValuesHolder objects whose values will be animated between over time. |

| Return ||
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [ValueAnimator](../android/animation/ValueAnimator.md)! | A ValueAnimator object that is set up to animate between the given values. |

### pause

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pause(): Unit
```  

### registerDurationScaleChangeListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun registerDurationScaleChangeListener(listener: ValueAnimator.DurationScaleChangeListener): Boolean
```

Registers a [DurationScaleChangeListener](../android/animation/ValueAnimator.DurationScaleChangeListener.md) This listens for changes to the system-wide scaling factor for Animator-based animations. Listeners will be called on the main thread.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [ValueAnimator.DurationScaleChangeListener](../android/animation/ValueAnimator.DurationScaleChangeListener.md):the listener to register. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the listener was registered. |

### removeAllUpdateListeners

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeAllUpdateListeners(): Unit
```

Removes all listeners from the set listening to frame updates for this animation. 

### removeUpdateListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeUpdateListener(listener: ValueAnimator.AnimatorUpdateListener!): Unit
```

Removes a listener from the set listening to frame updates for this animation.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [ValueAnimator.AnimatorUpdateListener](../android/animation/ValueAnimator.AnimatorUpdateListener.md)!:the listener to be removed from the current set of update listeners for this animation. |

### resume

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun resume(): Unit
```  

### reverse

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reverse(): Unit
```

Plays the ValueAnimator in reverse. If the animation is already running, it will stop itself and play backwards from the point reached when reverse was called. If the animation is not currently running, then it will start from the end and play backwards. This behavior is only set for the current animation; future playing of the animation will use the default behavior of playing forward. 

### setCurrentFraction

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCurrentFraction(fraction: Float): Unit
```

Sets the position of the animation to the specified fraction. This fraction should be between 0 and the total fraction of the animation, including any repetition. That is, a fraction of 0 will position the animation at the beginning, a value of 1 at the end, and a value of 2 at the end of a reversing animator that repeats once. If the animation has not yet been started, then it will not advance forward after it is set to this fraction; it will simply set the fraction to this value and perform any appropriate actions based on that fraction. If the animation is already running, then setCurrentFraction() will set the current fraction to this value and continue playing from that point. [Animator.AnimatorListener](../android/animation/Animator.AnimatorListener.md) events are not called due to changing the fraction; those events are only processed while the animation is running.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fraction` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The fraction to which the animation is advanced or rewound. Values outside the range of 0 to the maximum fraction for the animator will be clamped to the correct range. |

### setCurrentPlayTime

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCurrentPlayTime(playTime: Long): Unit
```

Sets the position of the animation to the specified point in time. This time should be between 0 and the total duration of the animation, including any repetition. If the animation has not yet been started, then it will not advance forward after it is set to this time; it will simply set the time to this value and perform any appropriate actions based on that time. If the animation is already running, then setCurrentPlayTime() will set the current playing time to this value and continue playing from that point.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `playTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time, in milliseconds, to which the animation is advanced or rewound. |

### setDuration

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDuration(duration: Long): ValueAnimator!
```

Sets the length of the animation. The default duration is 300 milliseconds.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `duration` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The length of the animation, in milliseconds. This value cannot be negative. |

| Return ||
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ValueAnimator](../android/animation/ValueAnimator.md)! | ValueAnimator The object called with setDuration(). This return value makes it easier to compose statements together that construct and then set the duration, as in`ValueAnimator.ofInt(0, 10).setDuration(500).start()`. |

### setEvaluator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEvaluator(value: TypeEvaluator<Any!>!): Unit
```

The type evaluator to be used when calculating the animated values of this animation. The system will automatically assign a float or int evaluator based on the type of`startValue`and`endValue`in the constructor. But if these values are not one of these primitive types, or if different evaluation is desired (such as is necessary with int values that represent colors), a custom evaluator needs to be assigned. For example, when running an animation on color values, the [ArgbEvaluator](../android/animation/ArgbEvaluator.md) should be used to get correct RGB color interpolation.

If this ValueAnimator has only one set of values being animated between, this evaluator will be used for that set. If there are several sets of values being animated, which is the case if PropertyValuesHolder objects were set on the ValueAnimator, then the evaluator is assigned just to the first PropertyValuesHolder object.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [TypeEvaluator](../android/animation/TypeEvaluator.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:the evaluator to be used this animation |

### setFloatValues

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFloatValues(vararg values: Float): Unit
```

Sets float values that will be animated between. A single value implies that that value is the one being animated to. However, this is not typically useful in a ValueAnimator object because there is no way for the object to determine the starting value for the animation (unlike ObjectAnimator, which can derive that value from the target object and property being animated). Therefore, there should typically be two or more values.

If there are already multiple sets of values defined for this ValueAnimator via more than one PropertyValuesHolder object, this method will set the values for the first of those objects.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `values` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):A set of values that the animation will animate between over time. |

### setFrameDelay

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setFrameDelay(frameDelay: Long): Unit
```

The amount of time, in milliseconds, between each frame of the animation. This is a requested time that the animation will attempt to honor, but the actual delay between frames may be different, depending on system load and capabilities. This is a static function because the same delay will be applied to all animations, since they are all run off of a single timing loop. The frame delay may be ignored when the animation system uses an external timing source, such as the display refresh rate (vsync), to govern animations. Note that this method should be called from the same thread that [start()](../android/animation/ValueAnimator.md))is called in order to have the new frame delay take effect on that animation. A runtime exception will be thrown if the calling thread does not have a Looper.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------|
| `frameDelay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the requested time between frames, in milliseconds |

### setIntValues

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIntValues(vararg values: Int): Unit
```

Sets int values that will be animated between. A single value implies that that value is the one being animated to. However, this is not typically useful in a ValueAnimator object because there is no way for the object to determine the starting value for the animation (unlike ObjectAnimator, which can derive that value from the target object and property being animated). Therefore, there should typically be two or more values.

If there are already multiple sets of values defined for this ValueAnimator via more than one PropertyValuesHolder object, this method will set the values for the first of those objects.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `values` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A set of values that the animation will animate between over time. |

### setInterpolator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInterpolator(value: TimeInterpolator!): Unit
```

The time interpolator used in calculating the elapsed fraction of this animation. The interpolator determines whether the animation runs with linear or non-linear motion, such as acceleration and deceleration. The default value is [android.view.animation.AccelerateDecelerateInterpolator](../android/view/animation/AccelerateDecelerateInterpolator.md)

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [TimeInterpolator](../android/animation/TimeInterpolator.md)!:the interpolator to be used by this animation. A value of`null`will result in linear interpolation. |

### setObjectValues

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setObjectValues(vararg values: Any!): Unit
```

Sets the values to animate between for this animation. A single value implies that that value is the one being animated to. However, this is not typically useful in a ValueAnimator object because there is no way for the object to determine the starting value for the animation (unlike ObjectAnimator, which can derive that value from the target object and property being animated). Therefore, there should typically be two or more values.

**Note:**The Object values are stored as references to the original objects, which means that changes to those objects after this method is called will affect the values on the animator. If the objects will be mutated externally after this method is called, callers should pass a copy of those objects instead.

If there are already multiple sets of values defined for this ValueAnimator via more than one PropertyValuesHolder object, this method will set the values for the first of those objects.

There should be a TypeEvaluator set on the ValueAnimator that knows how to interpolate between these value objects. ValueAnimator only knows how to interpolate between the primitive types specified in the other setValues() methods.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------|
| `values` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The set of values to animate between. |

### setRepeatCount

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRepeatCount(value: Int): Unit
```

Sets how many times the animation should be repeated. If the repeat count is 0, the animation is never repeated. If the repeat count is greater than 0 or [INFINITE](../android/animation/ValueAnimator.md), the repeat mode will be taken into account. The repeat count is 0 by default.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of times the animation should be repeated |

### setRepeatMode

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRepeatMode(value: Int): Unit
```

Defines what this animation should do when it reaches the end. This setting is applied only when the repeat count is either greater than 0 or [INFINITE](../android/animation/ValueAnimator.md). Defaults to [RESTART](../android/animation/ValueAnimator.md).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): [RESTART](../android/animation/ValueAnimator.md) or [REVERSE](../android/animation/ValueAnimator.md) Value is [android.animation.ValueAnimator#RESTART](../android/animation/ValueAnimator.md), or [android.animation.ValueAnimator#REVERSE](../android/animation/ValueAnimator.md) |

### setStartDelay

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStartDelay(startDelay: Long): Unit
```

The amount of time, in milliseconds, to delay starting the animation after [start()](../android/animation/ValueAnimator.md))is called. Note that the start delay should always be non-negative. Any negative start delay will be clamped to 0 on N and above.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| `startDelay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The amount of the delay, in milliseconds |

### setValues

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setValues(vararg values: PropertyValuesHolder!): Unit
```

Sets the values, per property, being animated between. This function is called internally by the constructors of ValueAnimator that take a list of values. But a ValueAnimator can be constructed without values and this method can be called to set the values manually instead.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `values` | [PropertyValuesHolder](../android/animation/PropertyValuesHolder.md)!:The set of values, per property, being animated between. |

### start

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun start(): Unit
```  

### toString

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### unregisterDurationScaleChangeListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun unregisterDurationScaleChangeListener(listener: ValueAnimator.DurationScaleChangeListener): Boolean
```

Unregisters a DurationScaleChangeListener.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [ValueAnimator.DurationScaleChangeListener](../android/animation/ValueAnimator.DurationScaleChangeListener.md):the listener to unregister. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the listener was unregistered. |

**See Also**

- [#registerDurationScaleChangeListener(DurationScaleChangeListener)](../android/animation/ValueAnimator.md))
